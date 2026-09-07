---
title: SlowBots
---

The Go build system supports "SlowBots", which are a way to configure the TryBots (pre-submit builders) to add additional builders into the set of build configurations that TryBots normally run.

Normally TryBots only run things that are fast and elastically provisioned. That is, TryBots run tests for ports that are available on Google Cloud where we have tons of capacity and can spin up many VMs at will, sharding out test execution widely so the TryBots complete in 5-10 minutes.

But sometimes that's not enough. SlowBots let you say that you're cool waiting a long time until some specific set of builders becomes available. (There is often only one physical machine for some configurations, and often backlogged with work, and that builder might be slow too.)

## Using SlowBots

Click "Choose Tryjobs" under the commit message and a dialog will appear.

![A red box indicating the location of the "Choose Tryjobs" button under the commit message.](https://github.com/golang/go/assets/1248668/5bfcb020-8cd2-4635-88a9-03efce4e69ba)

The dialog will ask you to click checkboxes for the builds you would like to run against your CL.
A typical CL to the main Go repo usually wants builders starting with `gotip-`.
[See below](#slowbot-names) for more details about the options.

![An example of the Choose Tryjobs dialog.](https://github.com/golang/go/assets/1248668/5fc635fb-e968-4e7e-b58c-960a09294b5b)

Once you select the builds you would like to run, there are two ways to trigger the test runs:

- **Blocking**: This is the recommended approach. Add the `Cq-Include-Trybots` git footer displayed in the dialog to the last paragraph of the commit message. For CL sent via github, it is OK to appear anywhere in the description of github PR. Once a patch set with the updated commit message is uploaded, vote `Commit-Queue+1` as usual. The additional builds are treated just like the default TryBots: failures will block submission and send email notifications, and the builds will automatically run on subsequent patch set (as long as the `Cq-Include-Trybots` line remains). Note that the `Cq-Include-Trybots` git footer will not be used if it's not in the last paragraph of the commit message. That is, it must be **right next to the `Change-Id` line without empty lines** (see screenshot below).
- **Advisory only**: Clicking the "Add" button will immediately start running the tests (even without a `Commit-Queue+1` vote). These are completely one-off advisory builds only. Status and results will appear in the "Checks" section (seen screenshot below), but failing results will not block submission or send an email notification. These builds will not automatically run again when a new patch set is uploaded.

![An example of how to use Cq-Include-Trybots](https://github.com/golang/go/assets/1248668/c4ede0cc-eb18-44a7-87e9-032f57f9a429)

### Reviewer workflow

As a reviewer, you cannot edit commit messages. If a CL you are reviewing should run SlowBots, we recommend the following workflow:

1. Select the desired builds in the "Choose Tryjobs" dialog.
2. Click "Add" to immediately start the builds.
3. Add an unresolved comment to the commit message asking the owner to add the exact `Cq-Include-Trybots` line from the dialog to the commit message.

(2) will provide immediate feedback from the results of the tests without waiting for the owner to upload a new patch set, while (3) will ensure that the tests continue running on future patch sets and block submission.

Note: https://crbug.com/40287467 tracks improvements to this process in LUCI to reduce toil.

### SlowBot names {#slowbot-names}

Each build's name roughly indicates what it will do, but below is some more detail:

- Builds may start with `x_$REPO` where `$REPO` is some module like `golang.org/x/$REPO` (such as `x_review-gotip-linux-amd64`). This build will run tests in that repository. If the CL is for the main Go repository, it will test the current `HEAD` of `$REPO` against that version of Go.
- If builds do not start with `x_$REPO` (like `gotip-linux-amd64`), they are testing the main Go repository (including the standard library and toolchain).
- Builds will then always list a Go version to build against, like `gotip` or `go1.21`. The former builds against the `master` branch of the main Go repository, while the latter builds against the `HEAD` of the corresponding release branch. If the CL is for `$REPO`, then `$REPO`'s tests will be run against `HEAD` of the corresponding main Go repository branch.
- Builds then list the OS and CPU architecture (specifically, the `GOOS` and `GOARCH`) to test against.
- Lastly, builds list some modifications, such as `gotip-linux-amd64-longtest-race`. Below is a list of some of the modifications and what they mean:
  - `longtest` runs the full suite of tests for the corresponding platform and repository.
  - `race` runs tests under the race detector.
  - `misccompile` will cross-compile all packages (including test packages) for all supported platforms as a smoke test. The platform for these builds is just the "host" platform for the cross-compilation.

**There are currently a lot more possible builds listed than what's actually supported or valid.**

Here are some general guidelines for which SlowBots will work as expected:

- If you're running SlowBots for a CL for one of the `golang.org/x/$REPO` repositories, then all the `x_$REPO-.*` builders will work as expected. Other builds will fail.
- If you're running SlowBots for a CL for the main Go repository, then every build that matches the branch the CL is for will work. For example, if you have a CL for the `master` branch, then every build with a name containing `gotip` will work as expected (`x_tools-gotip-linux-amd64`, `gotip-windows-amd64`, etc.). If you have a CL for the `release-branch.go1.21` branch, then every build with a name containing `go1.21` will work as expected (`x_tools-go1.21-linux-amd64`, `go1.21-windows-amd64`, etc.).

TODO: Apply these guidelines as filters automatically.

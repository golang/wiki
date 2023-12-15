---
title: Home
---

Welcome to the Go wiki, a collection of information about the [Go Programming Language](https://go.dev/). [Awesome Go](http://awesome-go.com/) is another great resource for Go programmers, curated by the Go community.

If you can't find what you need on this page, see the [list of all pages](All).

## Questions about Go

See [Questions](Questions).

Please do not ask questions by editing or creating a wiki page.  Any such changes will be silently reverted.

## Contributing

- This wiki is open to editing by any member of the Go community with a GitHub account.
- If you would like to add a new page, please first open an issue in the [Go issue tracker](https://github.com/golang/go/issues) with the prefix 'wiki' to propose the addition. Clearly state why the content does not fit into any of the existing pages.
- Because renaming of pages in the wiki can break external links, please open an issue before renaming or removing any wiki page.

# Table of Contents

- [Getting started with Go](#getting-started-with-go)
- [Working with Go](#working-with-go)
- [Learning more about Go](#learning-more-about-go)
- [The Go Community](#the-go-community)
- [Using the go toolchain](#using-the-go-toolchain)
- [Additional Go Programming Wikis](#additional-go-programming-wikis)
- [Online Services that work with Go](#online-services-that-work-with-go)
- [Troubleshooting Go Programs in Production](#troubleshooting-go-programs-in-production)
- [Contributing to the Go Project](#contributing-to-the-go-project)
- [Platform Specific Information](#platform-specific-information)
- [Release Specific Information](#release-specific-information)
- [Questions](Questions)

## Getting started with Go

- [The Go Tour](https://go.dev/tour/) is the best place to start.
- [Effective Go](https://go.dev/doc/effective_go) will help you learn how to write idiomatic Go code.
- [Go standard library documentation](https://pkg.go.dev/std) to familiarize yourself with the standard library.
- [Use the Go Playground](https://go.dev/play) to test out Go programs in your browser.
- Still not convinced? Check out this list of [Go Users](GoUsers) and a few of their [Success stories](SuccessStories). We've also assembled a long list of reasons [why you should give Go a try](WhyGo).
- Read about the companies which have [switched from other languages to Go](/wiki/FromXToGo).

## Working with Go

Ready to write some Go code of your own? Here are a few links to help you get started.

- Install and Setup your Environment
  - Start here: [Official Installation Documentation](https://go.dev/doc/install)
  - If you prefer to install from source, [read this first](https://go.dev/doc/install/source).
  - [InstallFromSource](InstallFromSource) - Additional tips on source installs.
  - Windows user? [Install and configure Go, Git, and Visual Studio Code for Windows](https://github.com/abourget/getting-started-with-golang)
  - Mac user? [How I start - Go](https://howistart.org/posts/go/1) - A step-by-step guide to installing Go and building your first web service.
  - Having installation problems? [InstallTroubleshooting](InstallTroubleshooting)
  - Make sure you have your [$GOPATH environment variable set correctly](https://go.dev/doc/install/source#gopath)
    - If you need additional tips on using [$GOPATH, go here](GOPATH).
- [Go IDEs and Editors](IDEsAndTextEditorPlugins) - Information on how to use your favorite editor with Go.
- [Tools for working with Go code](CodeTools) - Formatting, linting, vetting, refactoring, navigation, and visualization.
- Finding Go Libraries and Packages
  - Start here: [Go open source projects](Projects).
  - Search for Go packages: [pkg.go.dev](http://pkg.go.dev)
  - Visualization of the [Go open-source package graph](https://anvaka.github.io/pm/#/galaxy/gosearch?l=1)
- [Modules](Modules) - documentation on the dependency management system built into the Go command, added in 1.11.
- Publishing Go Packages as Open Source
  - Getting ready to publish your package? [Start here.](PackagePublishing)
  - [The Go Checklist](https://github.com/matttproud/gochecklist) - A comprehensive guide for publishing a project.
  - [Go Package, Go](https://johnsto.co.uk/blog/go-package-go) - A few recommendations for making Go packages easy to use.

## Learning more about Go

Once you have an overview of the language, here are resources you can use to learn more.

- [Learning Go](Learn) - A collection of resources for learning Go - beginner to advanced.
  - [Best Practices for a New Go Developer](https://www.cloudbees.com/blog/best-practices-for-a-new-go-developer) - Insights from Go community members.
  - [Server programming](LearnServerProgramming) - Building web, mobile, and API servers.
  - [More on concurrency](LearnConcurrency)
  - [More on error handling](LearnErrorHandling)
  - [More on testing](LearnTesting)
  - [More on mobile - Android and iOS](Mobile)
- [Books](Books) - A list of Go books that have been published (ebook, paper).
- [Blogs](Blogs) - Blogs about Go.
  - [Podcasts](Podcasts) - Podcasts and episodes featuring Go.
- Videos, Talks, and Presentations
  - [GopherVids](http://gophervids.appspot.com/) (currently unreachable) is a searchable index of videos about Go.
  - [GoTalks](GoTalks) - A collection of talks from Go conferences and meetups.
  - [Livestreams](Livestreams) - live interactive Go project streams with members of the community.
  - [Screencasts](Screencasts)
- [Articles](Articles) - A collection of articles to help you learn more about Go.
- [Training](Training) - Free and commercial, online, and classroom training for Go.
- [University Courses](Courses) - A list of CS programs and classes using Go.
- [Resources for non-English speakers](NonEnglish)

## The Go Community

Here are some of the places where you can find Gophers online. To get a sense of what it means to be a member of the Go community, read [Damian Gryski's keynote from the GolangUK 2015 conference](https://medium.com/@dgryski/the-go-community-f0d00e3a19e) or watch [Andrew Gerrand's closing keynote from GopherCon 2015](https://www.youtube.com/watch?v=0ht89TxZZnk).

- Where Gophers hangout online:
  - [The Go Forum](https://forum.golangbridge.org/) - An all-purpose discussion forum for the Go community.
  - [Gophers Slack Channel](http://gophers.slack.com/) - For real-time chat ([request membership](http://blog.gopheracademy.com/gophers-slack-community/)).
  - [Golang News](http://golangnews.com) - For curated links about Go Programming.
  - There is also a [/r/golang](http://reddit.com/r/golang) sub-reddit.
  - On Twitter, follow the [@golang](https://twitter.com/golang) account and keep tabs on the [#golang](https://twitter.com/search?q=%23golang&src=typd) hashtag.
  - We've also got a landing page on [Stack Overflow](http://stackoverflow.com/tags/go) for Go Q&A.
  - Matrix enthusiasts are invited to join [#Go:matrix.org](https://riot.im/app/#/room/#Go:matrix.org).
  - Discord users are welcome at the [Discord Gophers](https://discord.gg/golang) server.
  - Hashnode users talk and write about Go in [Hashnode Go community](https://hashnode.com/n/go).
- Mailing Lists
  - The mailing list for Go users is [golang-nuts](https://groups.google.com/forum/#!forum/golang-nuts) - very high traffic.
    - Before you post, [check to see if it's already been answered](http://stackoverflow.com/tags/go), then read [these tips on how to ask a good question](HowToAsk)
  - For discussions about the core Go open source project, join [golang-dev](https://groups.google.com/forum/#!forum/golang-dev).
  - To get just our release announcements, join [golang-announce](https://groups.google.com/forum/#!forum/golang-announce)
- User Groups & Meetups - There are [Go Meetups in many cities](http://www.meetup.com/find/?allMeetups=false&keywords=golang&radius=Infinity&userFreeform=Sunnyvale%2C+CA&mcId=z94086&mcName=Sunnyvale%2C+CA&sort=recommended&eventFilter=mysugg)
  - [GoBridge](http://golangbridge.org) - Volunteers helping underrepresented communities to teach technical skills and to foster diversity in Go.
  - [Women Who Go](http://www.womenwhogo.org/)
  - See here for [additional information GoUserGroups](GoUserGroups)
  - [GoDiscourse](https://github.com/godiscourse/godiscourse) - Go Discourse is an open-source Go-based forum from `hello world`.
- [Conferences](Conferences) - A list of upcoming and past Go conferences and major events.
- [Companies using Go](GoUsers) - A comprehensive list of companies using Go throughout the world.
- Learn more about the [Go Gopher images](Gopher) by Renee French.

## Using the Go Toolchain

- Start with the standard documentation for the `go` command [available here](https://pkg.go.dev/cmd/go/)
- Start here to learn about [vendoring](https://pkg.go.dev/cmd/go/#hdr-Vendor_Directories).
- [Cross Compilation](https://rakyll.org/cross-compilation/)
- Shared libraries and Go (buildmode)
  - [Go Shared Libraries](https://github.com/jbuberel/buildmodeshared) - Examples for creating and using shared libraries from Go and Python.
  - [Sharing Go Packages with C](http://blog.ralch.com/tutorial/golang-sharing-libraries/) - by [@ralch](https://twitter.com/ralch).
  - [Calling Go libraries from Python](https://blog.filippo.io/building-python-modules-with-go-1-5/) - by Filippo Valsorda
  - [Calling Go libraries from Ruby](http://c7.se/go-and-ruby-ffi/) - by Peter Hellberg
  - [Calling Go libraries from Swift](https://rakyll.org/swift/) - by Jaana Burcu Dogan
  - [Build a Ruby Gem with a Go native extension](http://blog.paracode.com/2015/08/28/ruby-and-go-sitting-in-a-tree) - by @jondot
  - [gohttplib](https://github.com/shazow/gohttplib) - An experiment in using Go 1.5 buildmode=c-shared.
- See the wikis below for additional details:
  - [GoGetTools](GoGetTools)
  - [GoGetProxyConfig](GoGetProxyConfig)
  - [cgo](cgo)
  - [CompilerOptimizations](CompilerOptimizations)
  - [GccgoCrossCompilation](GccgoCrossCompilation)
  - [GcToolchainTricks](GcToolchainTricks)
  - [GoGenerateTools](GoGenerateTools)
  - [Go Tooling Essentials](https://rakyll.org/go-tool-flags/) - by Jaana Burcu Dogan

## Additional Go Programming Wikis

- Concurrency
  - [Timeouts](Timeouts) - Abandon async calls that take too long
  - [LockOSThread](LockOSThread)
  - [MutexOrChannel](MutexOrChannel) - When to use one vs the other
- Working with Databases
  - [database/sql](http://go-database-sql.org/) - Online tutorial for working with the database/sql package.
  - [SQLDrivers](SQLDrivers)
  - [SQLInterface](SQLInterface)
- From other languages
  - [Go for Java Programmers](http://yourbasic.org/golang/go-java-tutorial/)
  - [Go for C++ Programmers](GoForCPPProgrammers)
- Strings
  - [GoStrings](GoStrings)
  - [String Matching](http://blog.gopheracademy.com/advent-2014/string-matching/)
- [Comments](Comments)
- [CommonMistakes](CommonMistakes)
- [Errors](Errors)
- [GcToolchainTricks](GcToolchainTricks)
- [InterfaceSlice](InterfaceSlice)
- [Iota](Iota)
- [MethodSets](MethodSets)
- [PanicAndRecover](PanicAndRecover)
- [Range](Range)
- [RateLimiting](RateLimiting)
- [SignalHandling](SignalHandling)
- [SimultaneousAssignment](SimultaneousAssignment)
- [SliceTricks](SliceTricks)
- [Switch](Switch)
- [TableDrivenTests](TableDrivenTests)

## Online Services that work with Go

If you're looking for services that support Go, here's a list to get you started.

- Cloud Computing - Go is well supported by most cloud service providers.
  - [Amazon Web Services](https://github.com/aws/aws-sdk-go)
  - [Azure](https://github.com/Azure/azure-sdk-for-go)
  - [DigitalOcean](https://github.com/digitalocean/godo)
  - [GE Predix](https://github.com/geaviation/goboot-starter)
  - [Google Cloud Platform for Go](https://cloud.google.com/go)
  - [Heroku](https://github.com/heroku/heroku-buildpack-go)
  - [IBM Bluemix](https://developer.ibm.com/bluemix/2015/10/28/getting-started-with-golang-on-bluemix/)
  - [OpenStack](https://github.com/openstack/golang-client)
  - [Vscale](https://github.com/vscale/go-vscale)
  - [Aliyun](https://github.com/aliyun/alibaba-cloud-sdk-go)
  - [Tencent](https://github.com/TencentCloud/tencentcloud-sdk-go)
  - See here for [information on additional providers](ProviderIntegration)
- [Continuous Integration and Continuous Deployment](HostedContinuousIntegration) - Go is well supported by most CI/CD frameworks
- Monitoring/Logging
  - [OpsDash](https://www.opsdash.com/) - Go-based cluster monitoring platform.
- Package and Dependency Management
  - [Gopkg.in](http://labix.org/gopkg.in) is a source for stable Go libraries, provided by Gustavo Niemeyer.

## Troubleshooting Go Programs in Production

- Understand the performance of your Go apps using the [pprof package](https://go.dev/blog/profiling-go-programs)
- Heap Dumps
  - [heapdump13](heapdump13)
  - [heapdump14](heapdump14)
  - [heapdump15-through-heapdump17](heapdump15-through-heapdump17)

## Contributing to the Go Project

- Start by reading the [Go Contribution Guidelines](https://go.dev/doc/contribute)
- If you'd like to propose a change to the Go project, start by reading the [Go Change Proposal Process](https://github.com/golang/proposal)
  - An archive of [design documents is also available](DesignDocuments)
- Go releases happen at ~6-month intervals. [See here for more information](Go-Release-Cycle)
- Want to know more about how the [Go source X-repositories are structured?](X-Repositories)
- The Go project requires that all code be reviewed before it is submitted.
  - Read more about our [code review practices](CodeReview)
  - If you're commenting on code under review, please read [these guidelines](CodeReviewComments)
- Issues
  - Bug reports and feature requests should be filed using the [GitHub issue tracker](https://github.com/golang/go/issues)
  - Want to understand how we [handle issues that are reported?](HandlingIssues)
- Project Dashboards
  - [Go Builds Dashboard info](DashboardBuilders)
  - [Performance Dashboard info](PerfDashboard)
  - [Download failed logs and debugging](/wiki/Download-build-farm-failed-logs-and-debugging)

## Platform Specific Information

See [MinimumRequirements](MinimumRequirements) for minimum platform requirements of current Go ports. Considering porting Go to a new platform? [Read our porting policy first](PortingPolicy).

- [ChromeOS](ChromeOS)
- [Darwin](Darwin)
- [DragonFly BSD](DragonFly-BSD)
- [FreeBSD](FreeBSD)
- [Go on ARM](GoArm)
- [Linux](Linux)
  - [Ubuntu](Ubuntu)
- [Mobile](Mobile)
- [NetBSD](NetBSD)
- [OpenBSD](OpenBSD)
- [Plan 9](Plan9)
- [Solaris](Solaris)
- [Windows](Windows)
  - [WindowsBuild](WindowsBuild)
  - [WindowsCrossCompiling](WindowsCrossCompiling)
  - [WindowsDLLs](WindowsDLLs)

Notes:

- Please refrain from changing the title of the wiki pages, as some of them might be linked to from [golang.org](https://golang.org) or other websites


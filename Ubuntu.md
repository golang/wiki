---
title: Ubuntu
---

> The Go project's official download page is at [https://go.dev/dl](https://go.dev/dl/).
>
> After downloading a binary release suitable for your system, you can install go by following the official installation instructions at [https://go.dev/doc/install](https://go.dev/doc/install#install).

There are some other options for Debian based systems like Ubuntu. These packages were not created by the Go project, and we don't support them, but they may be useful for you.

## Using PPA

If you're using Ubuntu (amd64, arm64 or armhf, LTS releases 18.04 or 20.04 or 22.04 or interim releases 23.04 or 23.10), then you can use the [longsleep/golang-backports PPA](https://launchpad.net/~longsleep/+archive/ubuntu/golang-backports) and update to Go 1.21.

```
sudo add-apt-repository ppa:longsleep/golang-backports
sudo apt update
sudo apt install golang-go
```

> **Note that `golang-go` installs latest Go as default Go. If you do not want that, install `golang-1.21` instead and use the binaries from `/usr/lib/go-1.21/bin`.**

## Using snap

Using [snaps](https://snapcraft.io/go) also works quite well.

```
sudo snap install --classic go
```
> A restart may or may not be required for the command to be recognized depending on your system.

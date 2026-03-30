# tobia-link releases

Binary releases for `tobia-link`, the local bridge used by Tobia mobile to
connect to your Codex sessions.

Simplified Chinese: [README.zh-CN.md](./README.zh-CN.md)

## What is `tobia-link`?

`tobia-link` runs on your development machine and:

- Connects to Tobia cloud relay
- Reads your local Codex project/session metadata
- Executes Codex requests coming from Tobia mobile

## Prerequisites

- A machine where Codex CLI is available and already authenticated
- Network access to your Tobia relay
- Tobia mobile app installed on your phone

## Quick Start

### macOS (Homebrew)

```bash
brew tap ihou/tobia
brew install tobia-link
tobia-link start
```

### Linux (manual install)

```bash
VERSION=v0.1.5
curl -fL -o tobia-link_${VERSION}_linux_amd64.tar.gz \
  https://github.com/ihou/tobia-link-releases/releases/download/${VERSION}/tobia-link_${VERSION#v}_linux_amd64.tar.gz
tar -xzf tobia-link_${VERSION}_linux_amd64.tar.gz
sudo install -m 0755 tobia-link /usr/local/bin/tobia-link
tobia-link start
```

### Windows

Use WSL2 (Ubuntu) and follow the Linux steps above inside WSL.

## Run

```bash
tobia-link start
```

Stop:

```bash
tobia-link stop
```

## Update

```bash
brew update
brew upgrade tobia-link
```

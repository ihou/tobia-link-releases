# tobia-link 发布仓库

这里存放 `tobia-link` 的二进制发布文件。  
`tobia-link` 是 Tobia 手机端连接本地 Codex 会话的桥接程序。

## `tobia-link` 是做什么的？

`tobia-link` 运行在你的开发机上，负责：

- 连接 Tobia 云中继
- 读取本地 Codex 项目/会话信息
- 执行来自手机端的 Codex 请求

## 前置条件

- 机器上已可使用 Codex CLI，并且已登录
- 可访问你的 Tobia relay
- 手机上已安装 Tobia 客户端

## 快速开始

### macOS（Homebrew）

```bash
brew tap ihou/tobia
brew install tobia-link
tobia-link start
```

### Linux（手动安装）

```bash
VERSION=v0.1.5
curl -fL -o tobia-link_${VERSION}_linux_amd64.tar.gz \
  https://github.com/ihou/tobia-link-releases/releases/download/${VERSION}/tobia-link_${VERSION#v}_linux_amd64.tar.gz
tar -xzf tobia-link_${VERSION}_linux_amd64.tar.gz
sudo install -m 0755 tobia-link /usr/local/bin/tobia-link
tobia-link start
```

### Windows

建议使用 WSL2（Ubuntu），在 WSL 中按 Linux 步骤安装和运行。

## 运行

```bash
tobia-link start
```

停止：

```bash
tobia-link stop
```

## 更新

```bash
brew update
brew upgrade tobia-link
```

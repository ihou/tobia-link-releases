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
tobia-link
```

### Linux（手动安装）

```bash
VERSION=v0.1.1
curl -fL -o tobia-link_${VERSION}_linux_amd64.tar.gz \
  https://github.com/ihou/tobia-link-releases/releases/download/${VERSION}/tobia-link_${VERSION#v}_linux_amd64.tar.gz
tar -xzf tobia-link_${VERSION}_linux_amd64.tar.gz
sudo install -m 0755 tobia-link /usr/local/bin/tobia-link
tobia-link
```

### Windows

建议使用 WSL2（Ubuntu），在 WSL 中按 Linux 步骤安装和运行。

## 配对流程

1. 启动 `tobia-link`
2. 在 Tobia 手机端扫码绑定
3. 使用期间保持 `tobia-link` 持续运行

在桌面环境下，`tobia-link` 默认会打开本地网页 UI；  
在纯命令行环境下，会在终端打印二维码。

## 常用命令

```bash
tobia-link           # 智能启动（桌面端打开 UI / 无桌面打印终端二维码）
tobia-link serve     # 只启动长连接转发
tobia-link ui        # 只启动本地网页 UI
tobia-link status    # 查看当前 agent 配置
```

## 更新

```bash
brew update
brew upgrade tobia-link
```

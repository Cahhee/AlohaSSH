<p align="center">
  <img src="icon.png" width="104" height="104" alt="AlohaSSH icon">
</p>

<h1 align="center">AlohaSSH</h1>

<p align="center">原生 macOS SSH 客户端 / Native macOS SSH client</p>

<p align="center">
  <a href="https://github.com/Cahhee/AlohaSSH/releases">下载 · Downloads</a> ·
  <a href="#english">English</a> ·
  <a href="PRIVACY.md">隐私政策 · Privacy</a> ·
  <a href="https://github.com/Cahhee/AlohaSSH/issues">问题反馈 · Issues</a>
</p>

AlohaSSH 是一款免费的 macOS SSH 客户端，支持多服务器管理、标签会话、左右分屏和文件传输。无需注册，没有订阅、广告或遥测。

界面使用 SwiftUI，SSH 连接使用系统 OpenSSH，终端由 SwiftTerm 渲染。支持 macOS 14 及以上版本，Apple Silicon 和 Intel Mac 使用同一个通用版安装包。

本仓库存放使用文档和发行版本，应用源码单独维护。

## 版本

1.2.1（构建 5）的安装包约 4 MB，已通过 Apple 公证。

**此版本目前仅保存在本地，尚未上传 GitHub Release。**

## 安装

版本发布后，可在 [Releases](https://github.com/Cahhee/AlohaSSH/releases) 下载。

1. 下载 `AlohaSSH-…-macOS-universal.zip` 并解压。
2. 将 `AlohaSSH.app` 拖入“应用程序”。
3. 打开应用，添加服务器，选择密码或私钥认证。

校验下载文件：

```sh
shasum -a 256 AlohaSSH-1.2.1-macOS-universal.zip
```

将结果与同版本的 `SHA256SUMS.txt` 对照。

首次连接需要核对服务器主机密钥指纹。访问已保存的凭据时，macOS 可能询问钥匙串授权。

## 功能

- **服务器管理**：分组、连接模板、批量添加与删除，可连接所选服务器或整个分组。
- **搜索与快速连接**：查找已保存节点，或输入 `user@host:port` 建立临时连接。
- **多会话与分屏**：左侧竖排标签，同一标签可左右分屏，分别连接同一台或不同服务器。切换标签不会清空终端内容或停止任务。
- **密码与私钥**：支持密码、私钥及加密私钥口令。重新输入密码并成功登录后，可更新保存的密码。
- **文件传输**：独立窗口浏览远程目录、上传和下载普通文件，支持 Finder 拖放与传输进度。
- **命令片段**：保存常用命令，执行前查看目标和内容；包含 root 会话配置公钥登录的预设。
- **本地终端**：打开 Mac 的登录 Shell，也可与远程终端并排显示。不需要开启系统远程登录。
- **外观与语言**：浅色、深色或跟随系统；简体中文和英语可即时切换。

`⌘W` 和主窗口关闭按钮只隐藏窗口，SSH、本地终端和文件传输继续运行。点击 Dock、菜单栏图标或按 `⌘0` 恢复窗口。

文件传输使用 SFTP 协议，服务器需启用 SFTP 子系统。目前不支持递归传输整个目录。命令片段使用独立 SSH 连接，不继承交互终端中的当前目录或临时环境。

## 快捷键

| 快捷键 | 操作 |
| --- | --- |
| `⌘N` | 添加服务器 |
| `⌘K` | 搜索节点／快速连接 |
| `⌘Return` | 连接所选服务器／新建对应会话 |
| `⌘T` | 新建本地终端 |
| `⌃Tab` / `⌃⇧Tab` | 切换下一个／上一个会话 |
| `⌘D` | 左右分屏 |
| `⌘⇧F` | 打开文件传输 |
| `⌘⇧P` | 打开命令片段 |
| `⌘W` | 隐藏主窗口，保留连接 |
| `⌘0` | 恢复主窗口 |
| `⌘,` | 设置 |
| `⌘Q` | 退出，按需确认正在运行的任务 |

## 隐私

AlohaSSH 不收集个人信息或使用数据，没有遥测、分析和广告 SDK。服务器配置保存在本机，密码、私钥和私钥口令保存在 macOS 系统钥匙串。SSH 和文件传输直接连接你指定的服务器。

详见 [隐私政策](PRIVACY.md)。提交问题前，请移除密码、私钥、真实服务器信息和敏感终端内容。

---

<a id="english"></a>

## English

AlohaSSH is a free macOS SSH client with server management, session tabs, split panes, and file transfers. It requires no account and includes no subscriptions, ads, or telemetry.

The app uses SwiftUI, system OpenSSH, and SwiftTerm. It runs on macOS 14 or later. One universal package supports Apple Silicon and Intel Macs. This repository contains documentation and releases; the app source is maintained separately.

### Version

Version 1.2.1 (build 5) is about 4 MB and is notarized by Apple.

**This version is currently saved locally and has not been uploaded to GitHub Releases.**

### Installation

Once published, downloads will be available under [Releases](https://github.com/Cahhee/AlohaSSH/releases).

1. Download and unzip `AlohaSSH-…-macOS-universal.zip`.
2. Drag `AlohaSSH.app` into Applications.
3. Open the app, add a server, and choose password or private-key authentication.

Run `shasum -a 256 <download.zip>` and compare the result with the release’s `SHA256SUMS.txt`.

Check the server’s host-key fingerprint on the first connection. macOS may ask for Keychain access when using saved credentials.

### Features

- Server groups, connection templates, batch setup and deletion, and group connections.
- Search saved servers or connect temporarily with `user@host:port`.
- Vertical session tabs and independent split panes. Switching tabs preserves terminal output and running tasks.
- Password and private-key authentication, including encrypted keys. Saved passwords can be updated after successful authentication.
- Remote file browsing, upload, download, Finder drag-and-drop, and transfer progress.
- Saved command snippets and a public-key login setup preset for root sessions.
- Local login shells, including beside remote terminals. macOS Remote Login is not required.
- Light, dark, and system appearance, with live English and Simplified Chinese switching.

`⌘W` and the main window’s close button hide the window while connections continue. Use the Dock, menu bar icon, or `⌘0` to restore it.

File transfers require the server’s SFTP subsystem. Recursive directory transfers are not supported. Command snippets use a separate SSH connection and do not inherit the interactive terminal’s working directory or temporary environment.

### Privacy

AlohaSSH collects no personal or usage data and includes no telemetry, analytics, or advertising SDKs. Server configurations stay on your Mac. Passwords, private keys, and key passphrases are stored in macOS Keychain. SSH and file transfers connect directly to the servers you specify.

See the [privacy policy](PRIVACY.md). Remove passwords, private keys, real server details, and sensitive terminal output before submitting an issue.

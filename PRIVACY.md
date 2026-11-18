# 隐私政策 / Privacy Policy

生效日期 / Effective date: 2026-11-18

## 简体中文

### 数据收集

AlohaSSH 不收集个人信息或使用数据，没有遥测、分析或广告 SDK，也不会自动向开发者上传崩溃日志。应用不统计启动次数、点击、连接时长、命令或终端输出，无需注册账号。

### 本地存储

| 资料 | 保存位置 |
| --- | --- |
| 服务器配置、分组、模板、命令片段、主机指纹 | 本机应用支持目录 |
| 密码、私钥、私钥口令 | macOS 系统钥匙串 |
| 语言、外观等设置 | 本机偏好设置 |

这些资料不会自动同步到开发者的服务器。

为供系统 SSH 使用，私钥可能被写入仅当前用户可访问的本地临时文件，连接结束后清理。命令片段以明文保存在本机，请勿在其中存放密码或私钥。

### 网络连接

SSH 和文件传输直接连接你指定的主机，不经过 AlohaSSH 中转。认证资料、命令、终端数据和文件会按连接需要传输给该服务器。远程服务器如何记录日志，由其运营者决定。

本地终端使用你的 Shell 配置。你运行的命令或程序可能自行联网。macOS 也可能联系 Apple 进行安全、签名或公证检查。这些行为不属于 AlohaSSH 遥测。

### GitHub 与问题反馈

本仓库、下载和 Issues 由 GitHub 提供。GitHub 可能处理账户信息、IP 地址、请求时间等信息，具体见 [GitHub 隐私声明](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)。

提交 Issue 时，你提供的内容会出现在公开仓库中。请先移除密码、私钥、真实服务器信息和敏感终端输出。

### 删除资料

你可以在应用中删除服务器和凭据，也可以手动删除本地应用资料，并通过“钥匙串访问”管理凭据。仅删除应用本身，可能仍会留下设置或钥匙串条目。

### 联系与更新

隐私问题可通过 [Issues](https://github.com/Cahhee/AlohaSSH/issues) 联系维护者。如果数据处理方式发生变化，我们会更新本文件和生效日期。

## English

### Data collection

AlohaSSH collects no personal or usage data. It includes no telemetry, analytics, or advertising SDKs and does not automatically upload crash reports to the developer. It does not record launches, clicks, connection duration, commands, or terminal output. No account is required.

### Local storage

| Data | Storage |
| --- | --- |
| Server configurations, groups, templates, command snippets, and host fingerprints | The local Application Support directory |
| Passwords, private keys, and key passphrases | macOS Keychain |
| Language, appearance, and other preferences | Local app preferences |

This data is not automatically synced to a developer server.

A private key may be written to a temporary local file restricted to the current user while system SSH needs it. The app cleans up the file when the connection ends. Command snippets are stored as plain text; do not put passwords or private keys in them.

### Network connections

SSH and file transfers connect directly to the host you specify, without an AlohaSSH relay. Authentication details, commands, terminal traffic, and files are sent to that server as needed. The server operator controls its logging.

Local terminals use your shell configuration. Commands and programs you run may make their own network requests. macOS may also contact Apple for security, signature, or notarization checks. These activities are separate from AlohaSSH telemetry.

### GitHub and issue reports

GitHub hosts this repository, downloads, and Issues. It may process account information, IP addresses, request times, and other information under its [privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

Issues submitted to this repository are public. Remove passwords, private keys, real server details, and sensitive terminal output before posting.

### Deleting data

You can delete servers and credentials in the app, remove local app data, and manage credentials through Keychain Access. Deleting the app alone may leave preferences or Keychain entries behind.

### Contact and updates

Contact the maintainer through [Issues](https://github.com/Cahhee/AlohaSSH/issues) for privacy questions. If the app’s data practices change, this file and its effective date will be updated.

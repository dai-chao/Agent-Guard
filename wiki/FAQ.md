# 常见问题（FAQ）

## 使用后一定不会被封号吗？

不会承诺这一点。Agent Guard 降低的是**可检测的环境与配置风险信号**；平台风控还涉及订阅、使用行为、设备与账号历史等多种因素。

## 扫描会不会上传我的配置？

不会。扫描与修复在本机完成，**数据不上云**。详见 [隐私与边界](Privacy)。

## 免费版和 Pro 有什么区别？

免费可扫可看指引；Pro 可一键自动修复并备份。见 [免费版与 Pro](Free-vs-Pro)。

## 支持哪些 Agent？

Claude Code、Cursor、Codex、Gemini、Windsurf、Hermes。检测项见 [检测项说明](Detection-Items)。

## 支持 Linux 吗？

暂不支持。当前支持 macOS（Apple Silicon / Intel）与 Windows x64。

## 一键修复会改坏我的代理吗？

可能会移除你写在 Shell / Agent 配置里的 proxy、`base_url` 等。修复前请阅读详情；Pro 会先备份到 `~/.agent-guard/backups/`。见 [修复指南](Repair-Guide)。

## 为什么出站 IP / 时区结果时好时坏？

VPN、节点切换、自动时区会导致指纹波动。建议在相对稳定的网络下复扫对比。

## 本仓库是开源的吗？

本仓库以产品说明与社区为主；客户端为专有软件，源码未在此开源。见 [隐私与边界](Privacy)。

## 在哪里提问？

见 [社区与反馈](Community)。

# 检测项说明

Agent Guard 扫描分两层：**通用环境**（所有 Agent 共享）与 **各产品合规画像**（按厂商风控差异定制）。

---

## 通用环境

| 检测项 | 说明 | 常见影响 |
|--------|------|----------|
| `timezone` | 系统 / Node 时区与推荐值比对 | 时区与账号常用地区不一致 |
| `timezone-auto` | 自动时区开关 | IP 变化时区跟随跳变，指纹不稳 |
| `system-proxy` | macOS 系统代理状态 | 系统级代理影响出站特征 |
| `shell-proxy` | `.zshrc` / `.bashrc` 等代理残留 | `HTTP(S)_PROXY` 等泄漏到 Agent 子进程 |
| `toolchain-proxy` | npm / pip 等工具链代理 | 包管理器代理污染开发环境 |
| `outbound-ip` | 出站 IP 类型与稳定性 | 机房 IP、共享节点、频繁跳变 |
| `timezone-ip-mismatch` | 时区与 IP 地理不一致 | 典型指纹冲突信号 |
| `fingerprint-score` | 浏览器 / 系统指纹评分 | 综合环境一致性评分 |

---

## 各产品合规画像

覆盖：Claude Code · Cursor · Codex · Gemini · Windsurf · Hermes

| 检测项 | 说明 | 典型位置 / 信号 |
|--------|------|-----------------|
| `config-leak` | 配置中 `proxy` / `base_url` 残留 | 各产品 `settings.json` 等 |
| `shell-env` | `ANTHROPIC_*` / `OPENAI_*` 等环境变量 | Shell 配置或进程环境 |
| `mcp-secrets` | MCP 配置明文 API Key | `mcp.json` 等 |
| `mcp-http` | MCP HTTP 端点风险 | 非可信 / 中转类 HTTP MCP |
| `api-endpoint` | 非官方 API 端点 | 自定义 base URL、第三方网关 |
| `relay-oauth` | OAuth 中转 / 第三方 Harness | 非官方登录与中转链路 |
| `state-footprint` | Claude 状态文件风险 | 主要针对 Claude Code |

具体命中项会在扫描结果中给出**路径、变量名与修复建议**。

---

## 风险类型对照

| 风险类型 | 相关检测（示例） |
|----------|------------------|
| 网络出口异常 | `outbound-ip`、`timezone-ip-mismatch` |
| 设备指纹不一致 | `timezone`、`fingerprint-score` |
| 配置与凭证泄漏 | `shell-env`、`config-leak`、`mcp-secrets` |
| 客户端身份异常 | `api-endpoint`、`relay-oauth` |

如何处理见 [修复指南](Repair-Guide)。

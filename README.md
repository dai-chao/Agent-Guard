# Agent Guard

本机 AI Agent **环境合规检测与修复** —— 发现代理泄漏、时区指纹不一致、配置残留、MCP 明文密钥等风控信号，降低账号封禁风险。

覆盖 Claude Code · Cursor · Codex · Gemini · Windsurf · Hermes

<p align="center">
  <a href="https://www.safeclaude.net/"><strong>官网 · 立即下载 →</strong></a>
</p>

<p align="center">
  <img src="https://download.safeclaude.net/8164e1c89188201096be1fe4826abae3.png" alt="Agent Guard 环境合规检测结果示意" width="680" />
</p>

---

## 为什么需要它？

2026 年起，Claude、Cursor、OpenAI 等平台的风控重点已从「单纯翻墙」转向 **订阅滥用、客户端身份校验与环境指纹**。多个弱信号叠加命中，账号可能在无人工复核的情况下被自动封禁。

Agent Guard 做的是**本机环境信号治理**，帮助你发现并清理高风险配置；不保证账号绝对安全。

| 风险类型 | 典型信号 | Agent Guard 怎么做 |
|----------|----------|-------------------|
| 网络出口异常 | 机房 IP、共享节点、IP 频繁跳变 | 检测出站 IP 类型与稳定性 |
| 设备指纹不一致 | 时区 / 语言 / 区域与 IP 不匹配 | 时区、指纹评分、地理一致性检查 |
| 配置与凭证泄漏 | Shell / Agent 配置里的 proxy、base_url、API Key | 配置残留与 MCP 明文密钥扫描 |
| 客户端身份异常 | 第三方 Harness、非官方 API 端点 | 端点与 OAuth 中转风险检测 |

---

## 核心能力

### 免费扫描本机环境

打开「环境合规」一键检测。**所有扫描数据留在本机，不上云。**

- **6** 款产品合规画像
- **20+** 环境风险信号
- **一键修复**（Pro）

### 分层扫描

**通用环境**（所有 Agent 共享）

| 检测项 | 说明 |
|--------|------|
| timezone / timezone-auto | 系统 · Node 时区比对；自动时区开关 |
| system-proxy | macOS 系统代理状态 |
| shell-proxy / toolchain-proxy | Shell 与 npm / pip 等代理残留 |
| outbound-ip | 出站 IP 类型与稳定性 |
| timezone-ip-mismatch | 时区与 IP 地理不一致 |
| fingerprint-score | 浏览器 / 系统指纹评分 |

**各产品合规画像**（按厂商风控差异定制）

| 检测项 | 说明 |
|--------|------|
| config-leak | 配置中 proxy / base_url 残留 |
| shell-env | `ANTHROPIC_*` / `OPENAI_*` 等环境变量 |
| mcp-secrets / mcp-http | MCP 明文密钥与 HTTP 端点风险 |
| api-endpoint | 非官方 API 端点 |
| relay-oauth | OAuth 中转 / 第三方 Harness |
| state-footprint | Claude 状态文件风险（Claude Code） |

### 发现问题，一键修复（Pro）

1. 点击「检测环境」→ 输出红 / 黄 / 绿合规灯与评分
2. 查看风险详情（路径、变量名、修复建议）
3. 一键修复：时区校正、清代理残留、清 Agent 配置……修复前自动备份到 `~/.agent-guard/backups/`
4. 重新扫描验证；无法自动修的项提供手动指引

> **免费版**：扫描 + 手动修复指引 · **Pro**：一键自动修复

### 附加：运行时 Hook 守护

可选能力，不改变「环境合规」主线：为 Cursor、Claude Code、Codex 等接入原生 Hook，高危操作弹窗审批，红线（如 `rm -rf /`、`curl | bash`）直接拒绝；含 40+ 规则、0–100 评分与攻击链检测。

---

## 系统要求

| 平台 | 说明 |
|------|------|
| macOS | Apple Silicon / Intel（x64） |
| Windows | x64 |
| Linux | 暂不支持 |

安装包与版本信息见 [官网下载页](https://www.safeclaude.net/)。

---

## 扫描与修复边界

**会做什么**

- 读取本机时区、系统代理、Shell / 工具链配置、已安装 Agent 的配置文件
- 检测出站 IP 类型与地理一致性（用于合规评分）
- Pro 可按确认结果自动修复部分项，并备份到 `~/.agent-guard/backups/`

**不会做什么**

- 不上传扫描结果或配置内容到云端
- 不在未确认的情况下静默改写系统或 Agent 配置
- 不替代官方客户端，也不提供账号、订阅或绕过风控的能力

---

## 下载与上手

1. 从 [safeclaude.net](https://www.safeclaude.net/) 下载并安装（环境扫描免费 · 一键修复需 Pro）
2. 打开应用 →「环境合规」→「检测环境」
3. 按提示处理高风险项；Pro 可一键修复后再次扫描验证

---

## 隐私承诺

- 扫描与修复均在 **本机** 完成
- **数据不上云**
- 自动修复前备份原配置，可随时回滚

---

## 交流群

扫码加入 Discord / Telegram，交流环境合规与使用问题：

<p align="center">
  <a href="https://discord.gg/vBqHjP2zs"><img src="https://download.safeclaude.net/discord-qr.png" alt="Discord" width="200" /></a>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://telegram.me/+q9F4tFkzsjY4ZTk1"><img src="https://download.safeclaude.net/telegram-qr.png" alt="Telegram" width="200" /></a>
</p>

<p align="center">
  <a href="https://discord.gg/vBqHjP2zs">Discord</a>
  &nbsp;·&nbsp;
  <a href="https://telegram.me/+q9F4tFkzsjY4ZTk1">Telegram</a>
</p>

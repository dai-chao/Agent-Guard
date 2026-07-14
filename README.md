# Agent Guard

**扫描本机环境，降低 AI 账号封号风险。**

本机 AI Agent **环境合规检测与修复** —— 一键发现代理泄漏、时区指纹不一致、配置残留、MCP 明文密钥等风控信号；覆盖 Claude Code、Cursor、Codex、Gemini、Windsurf、Hermes。发现问题可一键修复。

<p align="center">
  <a href="https://www.safeclaude.net/"><strong>官网 · 立即下载 →</strong></a>
  &nbsp;·&nbsp;
  <a href="https://www.safeclaude.net/">https://www.safeclaude.net/</a>
</p>


---

## 为什么需要它？

2026 年起，Claude、Cursor、OpenAI 等平台封号主因已从「单纯翻墙」转向 **订阅滥用、客户端身份校验与环境指纹**。多个弱信号叠加命中，账号可能在无人工复核的情况下被自动封禁。

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
时区 · 系统代理 · Shell / 工具链代理残留 · 出站 IP · 时区与 IP 地理不一致 · 指纹评分 …

**各产品合规画像**（按厂商风控差异定制）  
Claude Code · Cursor · Codex · Gemini · Windsurf · Hermes  
config 泄漏 · Shell 环境变量 · MCP 密钥 / HTTP · 非官方 API · OAuth 中转 …

### 发现问题，一键修复（Pro）

1. 点击「检测环境」→ 输出红 / 黄 / 绿合规灯与评分  
2. 查看风险详情（路径、变量名、修复建议）  
3. 一键修复：时区校正、清代理残留、清 Agent 配置……修复前自动备份到 `~/.agent-guard/backups/`  
4. 重新扫描验证；无法自动修的项提供手动指引  

> **免费版**：扫描 + 手动修复指引 · **Pro**：一键自动修复

### 运行时安全守护（附加）

环境合规之外，还可通过原生 Hook 实时监控 Agent 操作，形成「环境合规 + 行为审计」双重防护：

- 高危操作弹窗审批，红线（如 `rm -rf /`、`curl | bash`）直接拒绝  
- 40+ 安全规则与 0–100 安全评分  
- 攻击链检测（如「读 `.env` → 外传」「下载 → chmod → 执行」）

---

## 支持的产品

| Claude Code | Cursor | Codex | Gemini | Windsurf | Hermes |
|:-----------:|:------:|:-----:|:------:|:--------:|:------:|
| ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

---

## 下载

到官网获取最新安装包（macOS Apple Silicon / Intel · Windows）：

**[https://www.safeclaude.net/](https://www.safeclaude.net/)**

环境扫描免费 · 一键修复需 Pro · 数据不上云

---

## 三步上手

1. 从 [safeclaude.net](https://www.safeclaude.net/) 下载并安装  
2. 打开应用 → 进入「环境合规」→ 点击「检测环境」  
3. 按提示处理高风险项；Pro 用户可一键修复后再次扫描验证  

---

## 隐私承诺

- 扫描与修复均在 **本机** 完成  
- **数据不上云**  
- 自动修复前备份原配置，可随时回滚  


---

<p align="center">
  <strong>Agent Guard</strong> — 本机 AI Agent 环境合规检测与修复<br/>
  <a href="https://www.safeclaude.net/">https://www.safeclaude.net/</a>
</p>

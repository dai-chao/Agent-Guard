# 快速开始

## 1. 下载安装

前往官网获取安装包：https://www.safeclaude.net/#download（当前推荐 **v1.1.0**）

| 平台 | 安装包 |
|------|--------|
| macOS Apple Silicon | [AgentGuard-mac-arm64.dmg](https://download.safeclaude.net/1.1.0/AgentGuard-mac-arm64.dmg) |
| macOS Intel（x64） | [AgentGuard-mac-x64.dmg](https://download.safeclaude.net/1.1.0/AgentGuard-mac-x64.dmg) |
| Windows x64 | [AgentGuard-setup.exe](https://download.safeclaude.net/1.1.0/AgentGuard-setup.exe) |

Linux 暂不支持。详见 [系统要求](System-Requirements)。版本亮点见 [更新日志](Changelog)。

## 2. 第一次扫描（升级后也建议先做）

1. 打开 **Agent Guard**
2. 进入 **防封扫描**
3. 跑一轮完整检测
4. 等待扫描结束，查看：
   - 合规评分（0–100）
   - 红 / 黄 / 绿合规灯
   - 各项风险详情（路径、变量名、建议）

扫描数据留在本机，**不上云**。

## 3. 处理风险

| 版本 | 你可以做什么 |
|------|----------------|
| 免费版 | 查看详情 + 按手动指引自行修改 |
| Pro | 确认后一键自动修复，并备份原配置 |

**优先清红灯**：代理残留、配置泄漏、明文密钥、非官方端点。再看防护与隐私扫描。

修复流程见 [修复指南](Repair-Guide)。功能对比见 [免费版与 Pro](Free-vs-Pro)。

## 4. 复扫验证

修复后再次跑「防封扫描」，确认高风险项是否转为绿灯，并留一次底。无法自动修复的项会提供手动操作指引。

## 覆盖的产品

Claude Code · Cursor · Codex · Gemini · Windsurf · Hermes  

未安装的产品不会强行扫描其配置；已安装的会进入对应「合规画像」。

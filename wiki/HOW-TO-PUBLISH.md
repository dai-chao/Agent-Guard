# 如何发布到 GitHub Wiki

本目录是 Wiki 源稿。GitHub Wiki 是独立仓库，需单独推送。

## 1. 开启 Wiki

仓库 → **Settings** → **Features** → 勾选 **Wikis**

## 2. 推送页面

```bash
# 首次：克隆 wiki 仓库（需已在网页上创建过至少一页，或先手动 New Page）
git clone https://github.com/dai-chao/Agent-Guard.wiki.git
cd Agent-Guard.wiki

# 复制本目录全部 .md 到 wiki 仓库根目录
cp /path/to/Agent-Guard/wiki/*.md .

git add .
git commit -m "docs: 初始化 Agent Guard Wiki"
git push origin master   # 部分仓库默认分支为 main
```

## 3. 页面对照

| 文件 | Wiki 页面 |
|------|-----------|
| `Home.md` | 首页（必须） |
| `_Sidebar.md` | 左侧导航（自动生效） |
| `Changelog.md` | 更新日志 |
| 其余 `*.md` | 同名页面（`-` 连接多词标题） |

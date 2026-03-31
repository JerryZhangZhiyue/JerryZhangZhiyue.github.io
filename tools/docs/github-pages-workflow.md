# GitHub Pages 个人网站协作指南

## 1. 本地开发流程

```
写代码/改内容 → 本地预览 → 提交到 GitHub → 自动发布
```

### 1.1 常用命令

| 操作 | 命令 |
|------|------|
| 查看文件 | `ls`、`ls -la` |
| 查看当前状态 | `git status` |
| 添加文件到暂存区 | `git add 文件名` |
| 提交更改 | `git commit -m "说明"` |
| 推送到 GitHub | `git push` |
| 从 GitHub 拉取最新代码 | `git pull` |

### 1.2 完整提交流程

```bash
# 1. 查看改了什么
git status

# 2. 添加要提交的文件（. 表示所有文件）
git add .

# 3. 提交，写清楚做了什么
git commit -m "更新了首页介绍"

# 4. 推送到 GitHub
git push
```

---

## 2. Jekyll 本地预览

如果想在本地先预览效果：

```bash
# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 然后打开浏览器访问 http://localhost:4000
```

---

## 3. 工作原则

- **每次小改就提交**：不要攒很多改动一起提交，小步提交更容易追踪问题
- **提交信息要清楚**：说明"做了什么"而不是"改了文件"
- **推送前先拉取**：如果 GitHub 上有新的改动，先 `git pull` 再 `git push`

---

## 4. 常见问题

**Q: 推送后网站没更新？**
A: GitHub Pages 大约需要 1-2 分钟构建，稍等一下再刷新。

**Q: 提交信息写错了怎么办？**
A: 用 `git commit --amend` 可以修改最后一次提交信息（还没 push 的情况下）。

**Q: 想看更详细的 git 历史？**
A: 用 `git log --oneline --graph` 可以看到漂亮的提交历史图。

---

## 5. GitHub CLI (gh)

如果你装了 GitHub CLI，还可以用这些命令：

| 命令 | 说明 |
|------|------|
| `gh repo status` | 查看仓库状态 |
| `gh repo view` | 查看仓库信息 |
| `gh browse` | 在浏览器打开 GitHub 仓库页面 |

---

有问题随时问我！

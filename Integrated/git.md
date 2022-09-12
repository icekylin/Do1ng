- [Basic](#basic)
- [Repo](#repo)
- [Pull](#pull)
- [Push](#push)

---

## Basic

```bash
# 生成公钥与github连接
ssh-keygen
cat ~/.ssh/id_rsa.pub   # Github 新建 SSH keys 填入这里的内容
git config --global user.name "your_username"
git config --global user.email "your_email"
git config --list

# 建立仓库提示命令
echo "# Cyber-Security-Notes" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:kyl1n0/Cyber-Security-Notes.git
git push -u origin main
```

## Repo

```bash
# 重新绑定仓库（主要用于修改仓库名称后）
git remote rm origin
git remote add origin git@github.com:moekylin/Do1ng.git
```

## Pull

```bash
# 清除本地修改，拉取仓库最新内容
# 当本地仓库修改了内容执行 `git pull` 时，会出现如下内容，可以通过两种方式拉取远程仓库内容
error: Your local changes to the following files would be overwritten by merge:
        README.md
Please commit your changes or stash them before you merge.

## 方式 1：stash 会把所有未提交的修改（包括暂存的和非暂存的）都保存起来，用于后续恢复当前工作目录。比如下面的中间状态，通过git stash命令推送一个新的储藏，当前的工作目录就干净了。
git stash
git pull
git stash pop

## 方式 2: --hard 参数撤销工作区中所有未提交的修改内容，将暂存区与工作区都回到上一次版本，并删除之前的所有信息提交：
git reset --hard
git pull
```

## Push

```bash
# 撤销 (revert) 上一次 commit push
git log # 找到上一次 commit 的编号
git revert [commit编号] # 撤销上一次更改
git push

# 回滚 commit 到某一节点（同时删除仓库commit）
git log   # 找到想要回滚的 commit 编号
git reset --hard commit_id  # HEAD 指向此次提交记录
git push origin HEAD --force  # 强制 push

# 清除缓存重新提交数据 (用于更新.gitnore)
git rm --cached -r .
git add .
git commit -m "$(date)" # 当前时间的 commit
git push
```

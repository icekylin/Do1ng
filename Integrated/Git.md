- [基础命令](#基础命令)

## 基础命令

建立仓库提示命令
```git
echo "# Cyber-Security-Notes" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:kyl1n0/Cyber-Security-Notes.git
git push -u origin main
```

清除缓存重新提交数据(用于更新.gitnore):
```git
git rm --cached -r .
git add .
# 当前时间的 commit
git commit -m "$(date)"
```

重新绑定仓库（当修改了仓库地址时）
```
git remote rm origin
git remote add origin git@github.com:moekylin/blog.git
```

生成公钥与github连接
```
ssh-keygen
cat ~/.ssh/id_rsa.pub
git config --global user.name "moekylin"
git config --global user.email "moekylin@qq.com"
git config --list
```
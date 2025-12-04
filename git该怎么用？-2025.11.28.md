---
created: 2025-11-28
tags:
  - github
---
### 定义
- git是一个本地的版本控制工具，可以清晰追踪每一处修改，随时回滚版本，而且多人协作不会互相覆盖。

### 核心概念
- 仓库（Repo）：分为本地仓库和远程仓库（比如github）
- 提交（commit）
- 工作区：你正在编辑的文件
- 暂存区：add后添加到暂存区
- 本地仓库：所有修改记录都会保存到本地仓库。
- 远程仓库：push后就到了远程仓库。
- 分支：你可以在新分支上开发而不会影响到主分支，之后可以通过pull request合并到主分支。

- 初始化对应仓库：
```bash
# 在当前路径创建一个新的 Git 仓库
git init
# 关联远程仓库
git remote add origin https://github.com/amazinday/daily-output.git
```

- 初始化邮箱和用户名：

```bash
git config --global user.email "975514665@qq.com"

git config --global user.name "amazinday"
```

- 最核心的操作：
```bash
git add .
git commit -m "2025-11-28" 
git push origin main
```

- 常用操作：
```bash
# 添加所有改动的文件到暂存区(只包括改动和新增的文件)
git add .
git add 文件名.txt

# 把暂存区的文件正式保存为一次“提交”，执行后改动文件就被保存在本地git仓库中
# -m 后面跟提交信息
git commit -m ""
git commit # 不加-m会打开编辑器写详细说明

# 把改动提交到远程仓库
# origin:远程仓库的默认名
# main：主分支
git push origin main

# 取消所有暂存
git reset

# 查看提交历史
git log

# 修改最后一次提交(还没push)
git commmit --amend -m "新信息" # 修改提交信息

git add missing_file.txt
git commit --ament --no-edit # 补上文件

# 修改已push的文件信息
git commmit --amend -m "新信息"
git push --force origin main # 强制推送

# 设置上游，以后可以简写
git push -u origin main
git push # 之后

# 拉取到本地
git pull origin main

# 查看文件状态
git status

# 查看提交历史
git log

# 查看所有分支
git branch

# 创建并切换到新分支
git checkout -b 新分支名

# 合并指定分支到本分支
git merge 分支名

```
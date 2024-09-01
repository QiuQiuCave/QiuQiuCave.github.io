
1. 查看本地分支
如果你想查看所有本地分支，可以使用以下命令：

bash
复制代码
```git branch```

1. 创建新分支
如果你的意图是创建一个新的分支，可以使用以下命令：

bash
复制代码
git branch new-branch-name
将 new-branch-name 替换为你希望创建的分支名。

3. 切换到新分支
如果你想切换到新创建的分支，可以使用：

bash
复制代码
git checkout new-branch-name
或者，使用 git switch（更现代的方式）：

bash
复制代码
git switch new-branch-name
4. 检查远程分支
如果你想检查远程分支，可以使用：

bash
复制代码
git branch -r
5. 删除本地分支
如果你想删除本地分支，可以使用：

bash
复制代码
git branch -d branch-to-delete
6. 删除远程分支
如果你想删除远程分支，可以使用：

bash
复制代码
git push origin --delete branch-to-delete
总结
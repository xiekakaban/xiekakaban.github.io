---
title: github 命令合集
date: 2017-08-21 13:14:44
tags: [github]
---
----------------------------------------
## github 命令合集##

1. 关联用户：`$ git config –global user.name “yourName”`
2. 关联邮箱账号：`$ git config –global user.email “yourEmail”`
3. 创建新文件夹：`$ mkdir`
4. 显示当前目录：`$ pwd`
5. 将某个目录变成Git仓库：`$ git init`
6. 将文件添加到仓库：`$ git add`
7. 把文件提交到仓库，-m后面输入的是本次提交的说明：`$ git commit -m “wrote a readme file”`
8. 显示仓库当前的状态：`$ git status`
9. 查看文件的修改内容：`$ git diff`
10. 查看提交历史：`$ git log`
11. 单行显示提交历史：`$ git log –pretty=oneline`
12. 把当前版本回退到上一个版本：`$ git reset –hard HEAD^`
13. 查看 readme.txt 文件的内容：`$ cat readme.txt`
14. 回退到某一版本[例如3628164]：`$ git reset –hard 3628164`
15. 查看命令历史：`$ git reflog`
16. 查看文件工作区和版本库里最新版本的区别：`$ git diff HEAD –`
17. 丢弃文件工作区的修改：`$ git checkout –`
18. 把文件暂存区的修改回退到工作区：`$ git reset HEAD`
19. 删除文件：`$ rm`
20. 创建SSH Key：`$ ssh-keygen -t rsa -C “yourEmail”`
21. 建立本地仓库与GitHub远程仓库的关联：
```$ git remote add origin git@github.com:GitHubName/.git``` 
或者：```$ git remote add origin https://github.com/GitHubName/.git```
22. 把本地库的内容推送到远程，加-u参数，把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令：`$ git push -u origin master`
简化后的推送命令：$ git push origin master
23. 从GitHub远程仓库克隆：`$ git clone git@github.com:GitHubName/.git` 或者：`$ git clone https://github.com/GitHubName/.git`
24. 查看文件列表：`$ ls`
25. 创建“dev”分支：`$ git branch dev`
26. 切换到“dev”分支：`$ git checkout dev`
27. 创建“dev”分支并且切换到“dev”分支：`$ git checkout -b dev`
28. 列出所有分支，当前分支前面会标一个*号：`$ git branch`
29. 合并“dev”分支到当前分支：`$ git merge dev`
30. 删除dev分支：`$ git branch -d dev`
31. 用带参数的 git log 查看分支的合并情况：`$ git log –graph –pretty=oneline –abbrev-commit –no-ff`参数，表示禁用Fast forward，因为本次合并要创建一个新的commit，所以加上-m参数，把commit描述写进去：`$ git merge –no-ff -m “merge with no-ff” dev`
33. 把当前工作现场“储藏”起来：`$ git stash`
34. 查看储藏的工作现场列表：`$ git stash list`
35. 恢复“储藏”的工作现场同时把stash内容也删除：`$ git stash pop`
36. 恢复“储藏”的工作现场但不删除stash内容，需要用git stash drop来删除：`$ git stash apply`
37. 丢弃一个没有被合并过的“dev”分支：`$ git branch -D dev`
38. 查看远程库的信息：`$ git remote`
39. 查看远程库的详细信息：`$ git remote -v`
40. 推送“dev”分支到远程：`$ git push origin dev`
41. 在本地创建dev和远程分支对应的dev分支：`$ git checkout -b dev origin/dev`
42. 指定本地dev分支与远程origin/dev分支的链接：`$ git branch –set-upstream dev origin/dev`
43. 抓取分支：`$ git pull`
44. 打一个新标签v1.0：`$ git tag v1.0`
45. 查看所有标签：`$ git tag`
46. 对某一 commit id(例如6224937) 打标签：`$ git tag v0.9 6224937`
47. 查看v0.9标签信息：`$ git show v0.9`
48. 创建带有说明的标签，用-a指定标签名，-m指定说明文字，3628164为示例commit id：
`$ git tag -a v0.1 -m “version 0.1 released” 3628164`
49. 通过-s用私钥签名一个标签：`$ git tag -s v0.2 -m “signed version 0.2 released” fec145a`
50. 删除本地v0.1标签：`$ git tag -d v0.1`
51. 推送v1.0标签到远程：`$ git push origin v1.0`
52. 一次性推送全部尚未推送到远程的本地标签：`$ git push origin –tags`
53. 删除本地v0.9标签：`$ git tag -d v0.9`
54. 删除远程v0.9标签：`$ git push origin :refs/tags/v0.9`
55. 让Git显示颜色：`$ git config –global color.ui true`
56. 配置st为status的别名：`$ git config –global alias.st status`
# 推送至 Github

【参考】

- [Git创建本地仓库并推送至Github上（详细步骤）_git remote add "桥梁名称" 桥梁名称是什么-CSDN博客](https://blog.csdn.net/Rao_Limon/article/details/108418233)

# 修改全局属性

## 修改分支名

【参考】

- [git修改分支名称_git 修改分支名-CSDN博客](https://blog.csdn.net/weixin_49343190/article/details/121924241)
- [如何在 Git 中重命名本地或远程分支 (freecodecamp.org)](https://www.freecodecamp.org/chinese/news/how-to-rename-a-local-or-remote-branch-in-git)

# 切换分支而不改变本地代码

【参考】

- [git 学习笔记 —— 保留/丢弃当前分支修改并切换至其他分支 - yhjoker - 博客园 (cnblogs.com)](https://www.cnblogs.com/yhjoker/p/11776240.html)
- [git切换分支后，本地代码会改变吗_git checkout后 本地代码没变-CSDN博客](https://blog.csdn.net/weixin_45813802/article/details/129200139)

# 打印日志

【参考】

- 官方文档：[Git - git-log Documentation](https://git.github.io/git-scm.com/docs/git-log/zh_HANS-CN)
- [git log 使用及格式化参数详解_git log format-CSDN博客](https://blog.csdn.net/u011106915/article/details/105836289)

# 其他

## 操作本地仓库

【参考】[git教程1--如何操作本地仓库（保姆级教程，好上手）_gitlab-ce 本地仓库操作-CSDN博客](https://blog.csdn.net/TroyeSivanlp/article/details/121172010)

# 问题

1. 新创建仓库，git bash 中输入 `git branch`，为何不显示任何分支？

   回答：没有 commit 就没有分支，第一次 commit 后 git 自动创建 master 分支

   【参考】[git branch不显示本地分支的问题（二）_git branch -a没反应-CSDN博客](https://blog.csdn.net/qq_39671159/article/details/81261049)

2. 输入 `git commit` 后回车，为什么会打开 `COMMIT_EDITMSG` 文件？

   回答： git 的设置，该文件用来保存本次 commit 的信息、说明，等同于执行 `git commit -m`。打开 `COMMIT_EDITMSG` 的软件由 git 的 config 文件中的 `core.editor` 指定。

   【参考】

   - [为什么当我尝试在vscode中提交时，COMMIT_EDITMSG会打开？-腾讯云开发者社区-腾讯云 (tencent.com)](https://cloud.tencent.com/developer/ask/sof/107109436)
   - [git commit命令的使用与git默认编辑器的修改_git: use editor as commit input-CSDN博客](https://blog.csdn.net/longxiaowu/article/details/24017181)
   - 退出 vim 编辑器：[退出 .git/COMMIT_EDITMSG_git commit editmsg-CSDN博客](https://blog.csdn.net/qq_42770949/article/details/104974965)
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

### 图

`--graph` 选项**绘制一个 ASCII 图**，表示提交历史记录的分支结构。它通常与 `--oneline` 和 `--decorate` 命令结合使用，以便更容易查看哪个提交属于哪个分支：

```css
git log --graph --oneline --decorate
```

对于一个只有 2 个分支的简单存储库，这将产生以下结果：

```js
*   0e25143 (HEAD, main) Merge branch 'feature'
|\  
| * 16b36c6 Fix a bug in the new feature
| * 23ad9ad Start a new feature
* | ad8621a Fix a critical security issue
|/  
* 400e4b7 Fix typos in the documentation
* 160e224 Add the initial code base
```

星号显示提交在哪个分支上，因此上图告诉我们 `23ad9ad` 和 `16b36c6` 提交位于主题分支上，其余的都在 `main` 分支上。

虽然对于简单的存储库来说，这是一个不错的选择，但对于分支较多的项目，最好使用功能更全的可视化工具，比如 `gitk` 或 [Sourcetree](https://www.atlassian.com/zh/software/sourcetree)。

# 合并冲突

【参考】

- [使用命令行解决合并冲突 - GitHub 文档](https://docs.github.com/zh/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line)
- [如何解决 Git 中的合并冲突 (freecodecamp.org)](https://www.freecodecamp.org/chinese/news/resolve-merge-conflicts-in-git-a-practical-guide/)

# 分支管理规范

【参考】

- [Git 分支管理规范 | 前端规范 (woai3c.github.io)](https://woai3c.github.io/front-end-specification/git.html#git-分支管理规范)
- [Git 代码分支管理规范-腾讯云开发者社区-腾讯云 (tencent.com)](https://cloud.tencent.com/developer/article/1592957)
- [Git 的常规分支使用【dev和master】 - Yogic - 博客园 (cnblogs.com)](https://www.cnblogs.com/yogic/p/12764054.html)

# 其他

## 操作本地仓库

【参考】

- [git教程1--如何操作本地仓库（保姆级教程，好上手）_gitlab-ce 本地仓库操作-CSDN博客](https://blog.csdn.net/TroyeSivanlp/article/details/121172010)

## 操作远程仓库

【参考】

- [git教程2--远程仓库中的操作（保姆级教程，好上手)_gitlab保姆级教程-CSDN博客](https://blog.csdn.net/TroyeSivanlp/article/details/121173204)

# 问题

1. 新创建仓库，git bash 中输入 `git branch`，为何不显示任何分支？

   回答：没有 commit 就没有分支，第一次 commit 后 git 自动创建 master 分支

   【参考】[git branch不显示本地分支的问题（二）_git branch -a没反应-CSDN博客](https://blog.csdn.net/qq_39671159/article/details/81261049)

2. `git commit` 后显示 Author identity unknown

   回答：需要设置 git 的用户名和邮箱，设置本地的或全局的：

   - 设置邮箱：`git config --global 或 --local user.email`
   - 设置用户名：同上，最后一项换成 `user.name`

   【参考】[git使用commit命令后显示Author identity unknown的解决方法_unrecognized commit author in-CSDN博客](https://blog.csdn.net/qq_46036214/article/details/116275598)

3. 输入 `git commit` 后回车，为什么会打开 `COMMIT_EDITMSG` 文件？

   回答： git 的设置，该文件用来保存本次 commit 的信息、说明，等同于执行 `git commit -m`。打开 `COMMIT_EDITMSG` 的软件由 git 的 config 文件中的 `core.editor` 指定。

   【参考】

   - [为什么当我尝试在vscode中提交时，COMMIT_EDITMSG会打开？-腾讯云开发者社区-腾讯云 (tencent.com)](https://cloud.tencent.com/developer/ask/sof/107109436)
   - [git commit命令的使用与git默认编辑器的修改_git: use editor as commit input-CSDN博客](https://blog.csdn.net/longxiaowu/article/details/24017181)
   - 退出 vim 编辑器：[退出 .git/COMMIT_EDITMSG_git commit editmsg-CSDN博客](https://blog.csdn.net/qq_42770949/article/details/104974965)
# 官方文档：Github

包括 git 如何连接 github，如何连接本地仓库和远程仓库等。

【参考】[开始使用 Git - GitHub 文档](https://docs.github.com/zh/get-started/getting-started-with-git)

# 推送至 Github

【参考】

- [Git创建本地仓库并推送至Github上（详细步骤）_git remote add "桥梁名称" 桥梁名称是什么-CSDN博客](https://blog.csdn.net/Rao_Limon/article/details/108418233)

# 修改配置

## 全局配置

### 配置文件路径

【参考】[Window下Git的配置文件路径_git system配置文件路径-CSDN博客](https://blog.csdn.net/qq_28204343/article/details/109826754)

**`C:/User/Administor/.gitconfig`**

### 修改 core.editor

【参考】[Git - 配置 Git (git-scm.com)](https://git-scm.com/book/zh/v2/自定义-Git-配置-Git#_core_editor)

作用：指定默认编辑器，用来编辑提交信息。

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

## 图

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

## 其他

```bash
# 详细版
$ git log --graph --pretty=format:'%Cred%h%Creset -
%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative

# 简化版
$ git log --graph --oneline --decorate
```



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

### SSH 协议与 HTTPS 协议

【参考】

- [论git中使用https和ssh协议的区别 (cuiyongjian.com)](https://blog.cuiyongjian.com/engineering/git-https-ssh/)
- [【git】git中使用https和ssh协议的区别以及它们的用法 - WANNANANANA - 博客园 (cnblogs.com)](https://www.cnblogs.com/wannananana/p/12059806.html#:~:text=HTTPS利于匿名访问，适合开源项目，可以方便被别人克隆和读取,(但没有push权限)； SSH不利于匿名访问，比较适合内部项目，只要配置了SSH公钥极可自由实现clone和push操作。)

SSH 协议连接，配置了公钥后，可以免密码推送。

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

4. 输入 `ssh -T git@github.com` 后显示 `git@ip地址: Permission denied (publickey).`

   回答：原因可能有：

   - 没有将公钥（publickey）添加到本地 ssh 环境
   - 由于多日未进行 ssh 登陆操作，本地 publickey 失效

   【参考】

   - [Permission denied (publickey) 问题解决方法 && 解决Enter passphrase for key每次输入密码问题 - 掘金 (juejin.cn)](https://juejin.cn/post/6870436415734284301)
   - **【官方】**[错误：权限被拒绝（公钥） - GitHub 文档](https://docs.github.com/zh/authentication/troubleshooting-ssh/error-permission-denied-publickey)
   - **【官方】**[生成新的 SSH 密钥并将其添加到 ssh-agent - GitHub 文档](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
   - [Git报错解决：git@gitee.com: Permission denied (publickey).-腾讯云开发者社区-腾讯云 (tencent.com)](https://cloud.tencent.com/developer/article/1594769)

5. 输入 `ssh-add ~/.ssh/id_ed25519` 显示错误 `Could not open a connection to your authentication agent.`

   回答：

   1. 先检查现有 SSH 密钥

      输入 `ls -al ~/.ssh` 以查看是否存在现有的 SSH 密钥。

      【参考】[检查现有 SSH 密钥 - GitHub 文档](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys)

      如果没有就生成新的 SSH key

   2. 生成 SSH key

      ```bash
      ssh-keygen -t rsa -C "your_email@example.com"
      ```

      这将以提供的电子邮件地址为标签创建新 SSH 密钥。

      当系统提示您“Enter a file in which to save the key（输入要保存密钥的文件）”时，可以按 Enter 键接受默认文件位置。

      ```powershell
      > Enter file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]
      ```

      在提示符下，键入安全密码。 有关详细信息，请参阅“[使用 SSH 密钥密码](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases)”。

      ```shell
      > Enter passphrase (empty for no passphrase): [Type a passphrase]
      > Enter same passphrase again: [Type passphrase again]
      ```

   3. 打开 SSH 代理

      【参考】[生成新的 SSH 密钥并将其添加到 ssh-agent - GitHub 文档](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent)

      将这个 key 添加到ssh-agent中：

      ```bash
      $ ssh-agent -s
      # Agent pid 59566
      $ ssh-add ~/.ssh/id_rsa
      ```

       如果执行 `ssh-add` 时显示错误 `Could not open a connection to your authentication agent.` 那么执行

      ```bash
      eval `ssh-agent -s`
      ```

      后重新执行 ssh-add 那条命令即可。

      【参考】

      - 成功解决：[（诊断）为GitHub添加SSH key时出现“Could not open a connection to your authentication agent”错误的应对方案。 - 王智愚 - 博客园 (cnblogs.com)](https://www.cnblogs.com/Security-Darren/p/4106328.html)
      - [ssh公钥问题（Could not open a connection to your authentication agent.）-CSDN博客](https://blog.csdn.net/benisarookie/article/details/113114604)

6. 关联文本编辑器与 Git

   【参考】

   - 官方：[关联文本编辑器与 Git - GitHub 文档](https://docs.github.com/zh/get-started/getting-started-with-git/associating-text-editors-with-git)
   - [使用VSCode作为GIT默认编辑器_git 编辑时打开vscode-CSDN博客](https://blog.csdn.net/weixin_44225025/article/details/111410476)

   **【注意】**

   - 如果手动修改 `.gitconfig` 文件，git 会报错，提示 `fatal: bad config line 2 in file C:/Users/WYH/.gitconfig`

   - 如果按照官网，`core.editor "code --wait"`，则会打开旧版本的 VSCode，怀疑是根据环境配置来打开的：

     ```
     Version: 1.32.3 (system setup)
     Commit: a3db5be9b5c6ba46bb7555ec5d60178ecc2eaae4
     Date: 2019-03-14T22:49:40.955Z
     Electron: 3.1.6
     Chrome: 66.0.3359.181
     Node.js: 10.2.0
     V8: 6.6.346.32
     OS: Windows_NT ia32 10.0.19045
     ```

     因此，本地化修改为：

     ```bash
     $ git config --global core.editor "'E:\VSCode\Microsoft VS Code\bin\code' --wait"
     ```

     设置记事本为编辑器：

     ```bash
     $ git config --global core.editor "'C:/WINDOWS/system32/notepad.exe'"
     ```

     

   


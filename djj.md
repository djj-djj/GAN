# Git Command Line 学习笔记

[toc]
## Git 简介
**Git**（读作`/gɪt/`）是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。

**Git**是*Linus Torvalds*为了帮助管理*Linux*内核开发而开发的一个开放源码的版本控制软件。

> \* **版本控制**是一种记录一个或若干文件内容变化，以便将来查阅特定版本修订情况的系统。尽管 Git 通常用于软件源代码文件的版本控制，但实际上，你可以对任何类型的文件进行版本控制。
> 
> \*版本控制系统（VCS）可以帮助你保存某一文件的所有修订版本，有了它你就可以将某个文件回溯到之前的状态，甚至将整个项目都回退到过去某个时间点的状态，你可以比较文件的变化细节，查出最后是谁修改了哪个地方，从而找出导致怪异问题出现的原因，又是谁在何时报告了某个功能缺陷等等。使用版本控制系统通常还意味着，就算你乱来一气把整个项目中的文件改的改删的删，你也照样可以轻松恢复到原先的样子。但额外增加的工作量却微乎其微。 ***(Pro Git 2nd)***
>
>>版本控制系统：集中式 VS 分布式
参见 [Pro Git  2nd - About Version Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

Git 的辉煌历史就不在此赘述了（~~据说第一版 Git 只是 Linus 花了两周时间写的玩具项目~~），<u>Git 诞生不到一个月之内，Linux系统的源码已经由Git管理了。</u>

总而言之，Git 自诞生后便迅速获得大众的欢迎，尤其是 GitHub 网站上线后，Git 已经成为了目前最流行的分布式版本控制系统。


## Git 工作流程

Git 的一般工作流程如下：


1. 克隆 Git 资源作为工作目录。
2. 在克隆的资源上添加或修改文件。
3. 如果其他人修改了，你可以更新资源。
4. 在提交前查看修改。
5. 提交修改。
6. 在修改完成后，如果发现错误，可以撤 回提交并再次修改并提交。

![git-process-image](git-process.png "Git Process")

## Git 安装配置

  - [ ] 在使用 Git 前我们需要先安装 Git 客户端。 Git 各平台安装包下载地址为：http://git-scm.com/download

 - [x] 安装过程基本上使用默认配置即可，唯一的建议是选择使用 Visual Studio Code 作为默认编辑器。

安装完成后，我们需要配置 Git 仓库的个人的用户名称和电子邮件地址,打开 Git Bash，键入：
```bash
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
 ```  

设置完成后，你可以使用 `$ git config user.name` 和  `$ git config user.email`  来查看你设置的个人的用户名称和电子邮件地址


## 创建版本库

### 小结

- 初始化一个Git仓库，使用 git init 命令。
- 添加文件到Git仓库，分两步：
  - 使用命令 git add <file> 添加文件，可反复多次使用以添加多个文件；
  - 使用命令 git commit -m <message> 完成提交，可一次性提交多个文件。
   
---

## 附：Markdown 表格

|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |

|A|B|
|-|-|
|1|2|
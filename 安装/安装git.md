# Git安装教程（超详细）
### <font style="color:rgb(51, 51, 51);">一、前言</font>
<font style="color:rgb(51, 51, 51);">最近换了台新电脑，很多</font>[<font style="color:rgb(51, 51, 51);">软件</font>](https://marketing.csdn.net/p/3127db09a98e0723b83b2914d9256174?pId=2782&utm_source=glcblog&spm=1001.2101.3001.7020)<font style="color:rgb(51, 51, 51);">都需要重新安装，正好这几天也比较闲，那就记录一下 Git 的安装过程，温习温习。  
</font>[<font style="color:rgb(51, 51, 51);">Git</font>](https://edu.csdn.net/cloud/sd_summit?utm_source=glcblog&spm=1001.2101.3001.7020)<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">提供了一种有效的方式来管理项目的版本，协作开发，以及跟踪和应用文件的变化。它是开发者工具箱中必不可少的工具之一，广泛应用于软件开发和其他需要版本控制的领域。</font>

### <font style="color:rgb(51, 51, 51);">二、Git的安装</font>
#### <font style="color:rgb(51, 51, 51);">2.1Git的下载</font>
<font style="color:rgb(51, 51, 51);">Git下载地址为:  
</font><font style="color:rgb(51, 51, 51);">1.</font>[<font style="color:#2F8EF4;">git-scm.com</font>](https://git-scm.com/)<font style="color:rgb(51, 51, 51);">（官方，提供了各个平台（Windows、Mac、Linux）的安装程序）  
</font><font style="color:rgb(51, 51, 51);">2: </font>[<font style="color:#2F8EF4;">gitforwindows.org</font>](https://gitforwindows.org/)<font style="color:rgb(51, 51, 51);">（只有 windows 系统的安装包），  
</font><font style="color:rgb(51, 51, 51);">3.: </font>[<font style="color:#2F8EF4;">阿里镜像链接</font>](https://registry.npmmirror.com/binary.html?path=git-for-windows/)

#### <font style="color:rgb(51, 51, 51);">2.2Git的安装</font>
<font style="color:rgb(51, 51, 51);">本文安装的版本是</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">Git-2.43.0-64-bit.exe</font>

##### <font style="color:rgb(51, 51, 51);">2.2.1使用许可声明</font>
<font style="color:rgb(51, 51, 51);">双击下载后的</font><font style="color:rgb(51, 51, 51);">Git-2.43.0-64-bit.exe</font><font style="color:rgb(51, 51, 51);">，开始安装，这个界面主要展示了 GPL 第 2 版协议1的内容，点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846434701-1c7e0436-fb98-4771-86fb-735666a186d0.png)

##### <font style="color:rgb(51, 51, 51);">2.2.2 选择安装目录</font>
<font style="color:rgb(51, 51, 51);">最好点击 “Browse…” 更换目录，</font><font style="color:rgb(51, 51, 51);">尽量不要安装在C盘</font><font style="color:rgb(51, 51, 51);">。点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846434805-438bd22b-d146-4eaf-8c9b-2a6d4ef153ba.png)

##### <font style="color:rgb(51, 51, 51);">2.2.3 选择安装组件</font>
<font style="color:rgb(51, 51, 51);">图中这些英文都比较简单，我已经把大概意思翻译出来了，大家根据自己的需要选择勾选。</font><font style="color:rgb(51, 51, 51);">一般默认即可</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846434630-c8b485a8-d6f2-43c2-9581-c4d996f3b694.png)

##### <font style="color:rgb(51, 51, 51);">2.2.4 选择开始菜单文件夹</font>
<font style="color:rgb(51, 51, 51);">可以更改名称、不添加或者改到其他目录，</font><font style="color:rgb(51, 51, 51);">一般不动</font><font style="color:rgb(51, 51, 51);">；点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846434668-751efef0-0876-420d-ad55-32dec4bc6cf8.png)

##### <font style="color:rgb(51, 51, 51);">2.2.5 选择 Git 默认编辑器</font>
<font style="color:rgb(51, 51, 51);">选择Git使用的默认编辑器是指设置Git在执行某些需要打开编辑器的操作时，默认使用的文本编辑器。这些操作包括编写提交消息、解决合并冲突等。  
</font><font style="color:rgb(51, 51, 51);">默认的是vim编辑器，熟悉一点命令就会操作，没有</font><font style="color:rgb(51, 51, 51);">notepad</font><font style="color:rgb(51, 51, 51);">之类的简单，但是也不难，</font><font style="color:rgb(51, 51, 51);">使用默认的vim即可</font><font style="color:rgb(51, 51, 51);">；点击 [next] 进入下一步</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846441977-20badfc5-1bb5-4f2d-93de-a9bfc5b97866.png)

##### <font style="color:rgb(51, 51, 51);">2.2.6 决定初始化新项目(仓库)的主干名字</font>
<font style="color:rgb(51, 51, 51);">在最新的Git版本中，关于选择默认分支名称（Default Branch Name），有以下几个选项：  
</font><font style="color:rgb(51, 51, 51);">1.</font><font style="color:rgb(51, 51, 51);">让Git决定（Let Git decide）</font><font style="color:rgb(51, 51, 51);">： 这是Git 2.28版本之前的默认行为。即在创建新的仓库时，Git会使用默认的分支名称master。  
</font><font style="color:rgb(51, 51, 51);">2.覆盖新的默认分支名称（Override the default branch name for new repositories）： 由于技术和文化因素的考虑，Git 2.28版本引入了一个新的默认分支名称的选项。你可以将默认分支更改为其他名称（如main）。  
</font><font style="color:rgb(51, 51, 51);">这个选择哪个都可以，一般默认第一种，点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846436163-8ab21bb0-adc8-45bc-820e-22265081bf66.png)

##### <font style="color:rgb(51, 51, 51);">2.2.7 调整Git的环境变量</font>
<font style="color:rgb(51, 51, 51);">1.“</font>**<font style="color:rgb(51, 51, 51);">Use Git from Git Bash only</font>**<font style="color:rgb(51, 51, 51);">”（仅使用Git Bash中的Git）： 这是最谨慎的选择，因为它不会修改你的系统环境变量（PATH）。你只能在Git Bash中使用Git</font><font style="color:rgb(51, 51, 51);">命令行工具</font><font style="color:rgb(51, 51, 51);">。  
</font><font style="color:rgb(51, 51, 51);">2.“</font>**<font style="color:rgb(51, 51, 51);">Git from the command line and also from 3rd-party software</font>**<font style="color:rgb(51, 51, 51);">”（从命令行和第三方软件中使用Git）： 这是推荐的选项，它会将一些最基本的Git包装器添加到你的系统环境变量（PATH），以避免在环境中混乱地添加可选的Unix工具。你将能够从Git Bash、命令提示符和Windows</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">PowerShell</font><font style="color:rgb(51, 51, 51);">中使用Git，并且可以在PATH中寻找Git的任何第三方软件。  
</font><font style="color:rgb(51, 51, 51);">3.“</font>**<font style="color:rgb(51, 51, 51);">Use Git and optional Unix tools from the Command Prompt</font>**<font style="color:rgb(51, 51, 51);">”（从命令提示符中使用Git和可选的Unix工具）： 这个选项会将Git和可选的Unix工具都添加到你的系统环境变量（PATH）中。需要注意的是，这将覆盖Windows中的一些工具（如"find"和"sort"）。只有当你完全理解这些影响并愿意接受时，才应选择这个选项。  
</font><font style="color:rgb(51, 51, 51);">一般选择第二项</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846436366-5d5352c0-61b9-4ded-a978-ecf3eeaa4c22.png)

##### <font style="color:rgb(51, 51, 51);">2.2.8 选择 SSH 执行文件</font>
<font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846436432-9b4ee2bf-9116-4f8f-a471-12b2cb06d0d9.png)

##### <font style="color:rgb(51, 51, 51);">2.2.9 选择HTTPS后端传输</font>
<font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846436565-7ff2e9fb-818f-4236-9886-2d99ddbf600b.png)

##### <font style="color:rgb(51, 51, 51);">2.2.10 配置行尾符号转换</font>
<font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846437366-a49fe621-4c1c-4f1c-a8c5-9f1a96558832.png)

##### <font style="color:rgb(51, 51, 51);">2.2.11 配置终端模拟器以与 Git Bash 一起使用</font>
<font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846438005-33ed949a-59b9-4c7c-aaca-2764a33e1bdd.png)

##### <font style="color:rgb(51, 51, 51);">2.2.12 “git pull” 默认行为</font>
<font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846437982-7a60046d-033f-433c-9726-65047a34f57a.png)

##### <font style="color:rgb(51, 51, 51);">2.2.13 选择一个凭证帮助程序</font>
<font style="color:rgb(51, 51, 51);">这儿有两个选项：  
</font><font style="color:rgb(51, 51, 51);">1.</font>**<font style="color:rgb(51, 51, 51);">Git Credential Manager</font>**<font style="color:rgb(51, 51, 51);">： 使用跨平台的 Git Credential Manager（GCM）。Git Credential Manager 是一个凭据助手工具，可以帮助您在访问远程 Git 存储库时自动处理身份验证。它能够安全地存储并检索您的凭据。如果您选择此选项，Git 会配置使用 GCM 作为凭据助手。  
</font><font style="color:rgb(51, 51, 51);">2.</font>**<font style="color:rgb(51, 51, 51);">None</font>**<font style="color:rgb(51, 51, 51);">： 不使用凭据助手。如果您选择此选项，Git 将不会配置任何凭据助手，并在需要身份验证时，每次都会要求您手动输入凭据。  
</font><font style="color:rgb(51, 51, 51);">==如果您希望自动处理身份验证并避免频繁输入凭据，可以选择 Git Credential Manager。如果您更倾向于手动输入凭据或者使用其他凭据管理工具，则可以选择 None。==点击 [next] 进入下一步。</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846438091-e1123958-84d6-4bab-8165-76686c625aa2.png)

##### <font style="color:rgb(51, 51, 51);">2.2.14 配置额外的选项</font>
<font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，点击 [next] 进入下一步。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846439834-51c4ddc7-9b36-4207-865d-5a0a97ce0e9a.png)

##### <font style="color:rgb(51, 51, 51);">2.2.15 配置实验性选项</font>
<font style="color:rgb(51, 51, 51);">这是实验性功能，建议不开启。</font><font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">，直接点击 [install] 进行安装。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846442340-00b8a087-0926-4af6-b9be-2e93e12bdb3c.png)<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">安装中：  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846442371-672f8067-d770-422c-8466-984a21216629.png)

##### <font style="color:rgb(51, 51, 51);">2.2.16 安装完成</font>
<font style="color:rgb(51, 51, 51);">1.“Launch Git Bash”：启动 Git Bash 终端。  
</font><font style="color:rgb(51, 51, 51);">2.“View Release Notes”：查看版本说明。  
</font><font style="color:rgb(51, 51, 51);">使用默认配置</font><font style="color:rgb(51, 51, 51);">,点击[Finish]完成安装。</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846442318-8ce9a7ea-9b7b-45cf-aed9-08281ddba2e7.png)

#### <font style="color:rgb(51, 51, 51);">2.3 查看Git Bash终端和版本发行说明</font>
##### <font style="color:rgb(51, 51, 51);">2.3.1 Launch Git Bash</font>
<font style="color:rgb(51, 51, 51);">上一步勾选“Launch Git Bash”，即可打开Git Bash终端。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846442832-65e88925-2c26-4ebc-8813-55e676af00b0.png)

##### <font style="color:rgb(51, 51, 51);">2.3.2 View Release Notes</font>
<font style="color:rgb(51, 51, 51);">上一步勾选“View Release Notes”，即可跳转此网页。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846444366-f0b13999-d0f2-4f81-9176-a4e251a6bd56.png)

#### <font style="color:rgb(51, 51, 51);">2.4 Git的功能简介</font>
<font style="color:rgb(51, 51, 51);">在 Windows 安装好的 Git 上，您会得到以下功能： Git Bash、Git CMD、Git FAQs、Git GUI、Git Release Note，下面就分别介绍一下这几个。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846444343-f779563a-ff64-4b42-bfbe-987de5a08aef.png)

##### <font style="color:rgb(51, 51, 51);">2.4.1 Git Bash (同2.3.1 Launch Git Bash)</font>
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846444847-fd9b25fc-e720-4f7f-9b31-65c9bd6a61b4.png)

##### <font style="color:rgb(51, 51, 51);">2.4.2 Git CMD</font>
**<font style="color:rgb(51, 51, 51);">描述</font>**<font style="color:rgb(51, 51, 51);">： Git CMD 是一个在 Windows 命令提示符中运行的命令行工具。与 Git Bash 不同，Git CMD 更接近于 Windows 命令行环境。  
</font>**<font style="color:rgb(51, 51, 51);">用途</font>**<font style="color:rgb(51, 51, 51);">： 类似于 Git Bash，Git CMD 也允许用户在命令行中执行 Git 命令，进行版本控制操作。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846445462-772f2c73-9277-49de-b7f6-7385d87bc8cf.png)

##### <font style="color:rgb(51, 51, 51);">2.4.3 Git FAQs</font>
**<font style="color:rgb(51, 51, 51);">描述</font>**<font style="color:rgb(51, 51, 51);">： Git FAQs（Frequently Asked Questions）包含常见问题和解答，是一份常见问题的集合，为用户提供了解决常见问题的参考资料。  
</font>**<font style="color:rgb(51, 51, 51);">用途</font>**<font style="color:rgb(51, 51, 51);">： 用户可以在 Git FAQs 中查找关于 Git 的常见问题的答案，以解决遇到的问题。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846445349-51f06ea2-bc32-4fad-a380-9b8f24c34e78.png)

##### <font style="color:rgb(51, 51, 51);">2.4.4 Git GUI</font>
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846452049-b6118f96-4968-40f7-b0f7-bb8990687d00.png)

##### <font style="color:rgb(51, 51, 51);">2.4.5 Git Release Note （同2.3.2 View Release Notes）</font>
**<font style="color:rgb(51, 51, 51);">描述</font>**<font style="color:rgb(51, 51, 51);">： Git Release Note 包含了每个 Git 版本的发布说明，记录了每个版本的新功能、改进和修复的问题等信息。  
</font>**<font style="color:rgb(51, 51, 51);">用途</font>**<font style="color:rgb(51, 51, 51);">： 用户可以通过查阅 Git Release Note 了解每个 Git 版本的更新内容，以了解新功能、改进和潜在的问题。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846454124-665b3be2-755f-4c87-84f8-38fa47eae400.png)

### <font style="color:rgb(51, 51, 51);">三、Git的基本使用</font>
#### <font style="color:rgb(51, 51, 51);">3.1 基本的名词和概念</font>
<font style="color:rgb(51, 51, 51);">Git 中有一些基本的名词和概念，理解这些名词有助于正确使用 Git 进行版本控制。以下是一些基本的 Git 名词：</font>

1. **<font style="color:rgb(51, 51, 51);">仓库（Repository）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">一个 Git 仓库是项目的存储空间，包含项目文件和版本历史记录。可以是本地仓库（Local Repository）或远程仓库（Remote Repository）。</font>
2. **<font style="color:rgb(51, 51, 51);">工作区（Working Directory）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">工作区是你在电脑上能看到的项目目录，包含项目文件和子文件夹。</font>
3. **<font style="color:rgb(51, 51, 51);">暂存区（Staging Area）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">暂存区是一个中间区域，用于存放将要提交的修改。在提交前，你需要将修改先添加到暂存区。</font>
4. **<font style="color:rgb(51, 51, 51);">提交（Commit）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">提交是对工作区和暂存区的修改进行保存的操作。每次提交都有一个唯一的标识符（哈希值），并包含了修改的描述信息。</font>
5. **<font style="color:rgb(51, 51, 51);">分支（Branch）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">分支是项目的一个工作线，可以创建新的分支用于开发新功能或修复 bug，然后将其合并回主分支。</font>
6. **<font style="color:rgb(51, 51, 51);">主分支（Main/Branch）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">主分支是项目的默认分支，通常被称为</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">master</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">或</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">main</font>`<font style="color:rgb(51, 51, 51);">，是项目的主要开发线。</font>
7. **<font style="color:rgb(51, 51, 51);">远程仓库（Remote Repository）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">远程仓库是托管在网络上的项目副本，可以在 GitHub、GitLab、Bitbucket 等平台上进行多人协作。</font>
8. **<font style="color:rgb(51, 51, 51);">克隆（Clone）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">克隆是从远程仓库复制整个项目到本地，创建一个本地仓库的副本。</font>
9. **<font style="color:rgb(51, 51, 51);">拉取（Pull）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">拉取是从远程仓库获取最新修改，将远程仓库的变化更新到本地。</font>
10. **<font style="color:rgb(51, 51, 51);">推送（Push）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">推送是将本地的修改上传到远程仓库，使得远程仓库也包含最新的工作。</font>
11. **<font style="color:rgb(51, 51, 51);">合并（Merge）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">合并是将不同分支的修改合并到一起，通常用于将新功能或修复的代码合并回主分支。</font>
12. **<font style="color:rgb(51, 51, 51);">冲突（Conflict）：</font>**<font style="color:rgb(51, 51, 51);">  
</font><font style="color:rgb(51, 51, 51);">冲突发生在合并分支时，表示有两处或多处修改互相冲突，需要手动解决。</font>

<font style="color:rgb(51, 51, 51);">上面的基本名词构成了 Git 的核心概念，了解它们有助于更好地理解和使用 Git 进行版本控制。</font>

#### <font style="color:rgb(51, 51, 51);">3.2 用的命令和操作步骤</font>
<font style="color:rgb(51, 51, 51);">Git 的使用涉及到一系列命令和操作，以下是一份简单的 Git 使用指南，包含了常用的命令和操作步骤：</font>

<font style="color:rgb(51, 51, 51);">1.初始化一个新仓库</font>

```bash
git init
```

<font style="color:rgb(51, 51, 51);">2.克隆远程仓库</font>

```bash
git clone <远程仓库地址>
```

<font style="color:rgb(51, 51, 51);">3.配置用户信息</font>

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

<font style="color:rgb(51, 51, 51);">4.查看项目状态</font>

```bash
git status
```

<font style="color:rgb(51, 51, 51);">5.添加文件到暂存区</font>

```bash
git add <文件名>
```

<font style="color:rgb(51, 51, 51);">6.提交更改</font>

```bash
git commit -m "提交描述"
```

<font style="color:rgb(51, 51, 51);">7.查看提交历史</font>

```bash
git log
```

<font style="color:rgb(51, 51, 51);">8.创建分支</font>

```bash
git branch <分支名>
```

<font style="color:rgb(51, 51, 51);">9.切换分支</font>

```bash
git checkout <分支名>
```

<font style="color:rgb(51, 51, 51);">10.合并分支</font>

```bash
git merge <被合并的分支名>
```

<font style="color:rgb(51, 51, 51);">11.查看远程仓库信息</font>

```bash
git remote -v
```

<font style="color:rgb(51, 51, 51);">12.拉取远程仓库的变化</font>

```bash
git pull origin <分支名>
```

<font style="color:rgb(51, 51, 51);">13.推送本地修改到远程仓库</font>

```bash
git push origin <分支名>
```

<font style="color:rgb(51, 51, 51);">14.克隆并创建分支</font>

```bash
git clone <远程仓库地址> -b <分支名>
```

<font style="color:rgb(51, 51, 51);">15.解决冲突</font>

+ <font style="color:rgb(51, 51, 51);">在合并中可能会发生冲突，需要手动解决冲突后再提交。</font>

<font style="color:rgb(51, 51, 51);">16.创建标签</font>

```bash
git tag -a <标签名> -m "标签描述" <提交的哈希值>
```

<font style="color:rgb(51, 51, 51);">17.查看远程分支</font>

```bash
git branch -r
```

<font style="color:rgb(51, 51, 51);">18.恢复工作区到指定版本</font>

```bash
git checkout <版本号> -- <文件名>
```

<font style="color:rgb(51, 51, 51);">这只是 Git 常见操作的一小部分，实际使用中可能会涉及到更多的命令和场景。建议在使用 Git 前，先学习一些基础概念，然后通过实际操作逐步深入。 Git 的强大之处在于其灵活性和丰富的功能，可以适应各种开发场景。</font>

<font style="color:rgb(51, 51, 51);">  
</font>


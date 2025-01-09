# nvm安装、配置与使用详解
### <font style="color:rgb(51, 51, 51);">一.</font><font style="color:rgb(51, 51, 51);">nvm</font><font style="color:rgb(51, 51, 51);">介绍</font>
`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">全称为</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">node.js version management</font>`<font style="color:rgb(51, 51, 51);">，顾名思义是用于管理多个 nodejs 的</font>[<font style="color:rgb(51, 51, 51);">版本控制</font>](https://edu.csdn.net/cloud/sd_summit?utm_source=glcblog&spm=1001.2101.3001.7020)<font style="color:rgb(51, 51, 51);">工具。通过 nvm 可以安装和切换不同版本的 nodejs。</font>

### <font style="color:rgb(51, 51, 51);">二.安装nvm</font>
+ <font style="color:rgb(51, 51, 51);">在下载</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">前需先把之前安装的</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">卸载。</font>

[<font style="color:rgb(51, 51, 51);">nvm官网下载地址</font>](https://github.com/coreybutler/nvm-windows/releases)<font style="color:rgb(51, 51, 51);">：</font>[https://gitcode.com/gh_mirrors/nv/nvm-windows/releases?utm_source=csdn_github_accelerator](https://gitcode.com/gh_mirrors/nv/nvm-windows/releases?utm_source=csdn_github_accelerator)

<font style="color:rgb(51, 51, 51);">1.选择</font>`<font style="color:rgb(51, 51, 51);">nvm-setup.eve</font>`<font style="color:rgb(51, 51, 51);">进行安装。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846124004-860e4070-d85e-4da9-9f96-611ab2249e6e.png)

<font style="color:rgb(51, 51, 51);">2.选择</font>`<font style="color:rgb(51, 51, 51);">Iaccept the afreement</font>`<font style="color:rgb(51, 51, 51);">之后点击</font>`<font style="color:rgb(51, 51, 51);">Next</font>`<font style="color:rgb(51, 51, 51);">。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846123860-b881e48e-c524-4160-9222-ad0bf6602f7e.png)

<font style="color:rgb(51, 51, 51);">3.点击</font>`<font style="color:rgb(51, 51, 51);">Browse...</font>`<font style="color:rgb(51, 51, 51);">可以选择</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的安装目录，我这里就选择默认安装到C盘，再点击</font>`<font style="color:rgb(51, 51, 51);">Next</font>`<font style="color:rgb(51, 51, 51);">进行下一步。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846124158-2a40ccde-8748-4d0d-a714-e956b03f3296.png)

<font style="color:rgb(51, 51, 51);">4.点击</font>`<font style="color:rgb(51, 51, 51);">Browse...</font>`<font style="color:rgb(51, 51, 51);">可以选择</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">的安装目录，我这里就选择默认安装到C盘，再点击</font>`<font style="color:rgb(51, 51, 51);">Next</font>`<font style="color:rgb(51, 51, 51);">进行下一步。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846123844-42ea06e8-17dc-49b6-973a-056bf176d0b0.png)

<font style="color:rgb(51, 51, 51);">5.完成第4步之后呢只需要再点击</font>`<font style="color:rgb(51, 51, 51);">Install</font>`<font style="color:rgb(51, 51, 51);">就可以进行</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的安装。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846123808-6faf8492-4f63-4879-a5c1-29f95fd0e842.png)

<font style="color:rgb(51, 51, 51);">6.安装完成后我们可以打开命令提示符</font>`<font style="color:rgb(51, 51, 51);">cmd</font>`<font style="color:rgb(51, 51, 51);">或</font>`<font style="color:rgb(51, 51, 51);">PowerShell</font>`<font style="color:rgb(51, 51, 51);">，验证</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">是否安装成功  
</font><font style="color:rgb(51, 51, 51);">使用快捷键</font>`<font style="color:rgb(51, 51, 51);">Win+R</font>`<font style="color:rgb(51, 51, 51);">按</font>`<font style="color:rgb(51, 51, 51);">Win</font>`<font style="color:rgb(51, 51, 51);">键和</font>`<font style="color:rgb(51, 51, 51);">R</font>`<font style="color:rgb(51, 51, 51);">键，调出"运行"对话框，然后输入</font>`<font style="color:rgb(51, 51, 51);">cmd</font>`<font style="color:rgb(51, 51, 51);">并按"确定"。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846125423-b886aa4f-f0ee-4e12-beba-e4021d878a5e.png)

<font style="color:rgb(51, 51, 51);">7.打开</font>`<font style="color:rgb(51, 51, 51);">cmd</font>`<font style="color:rgb(51, 51, 51);">后输入</font>`<font style="color:rgb(51, 51, 51);">nvm -v</font>`<font style="color:rgb(51, 51, 51);">如果安装成功的话会看到</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的版本号</font><font style="color:rgb(51, 51, 51);"> </font>nvm常用命令在本文下方<font style="color:rgb(51, 51, 51);">。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846125441-5f891dc9-3018-4821-b62e-2f2f741fd5fa.png)

### <font style="color:rgb(51, 51, 51);">三.nvm的配置</font>
+ <font style="color:rgb(51, 51, 51);">到这里</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的安装就已经结束了、现在来配置</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的镜像源和环境变量。</font>

<font style="color:rgb(51, 51, 51);">1.找到我们的此电脑右击打开点击属性。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846125548-c1b3460a-d213-49e5-8dbd-25e7c4fe2df2.png)

<font style="color:rgb(51, 51, 51);">2.下滑找到高级系统设置。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846125514-31f48a59-19d1-4d98-9914-675747eeb630.png)

<font style="color:rgb(51, 51, 51);">3.点击环境变量。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846125586-fea3749d-77d5-456c-9f93-c6dbb1ec2b8e.png)

<font style="color:rgb(51, 51, 51);">4.找到我们的用户变量和系统变量查看</font>`<font style="color:rgb(51, 51, 51);">NVM_HOME</font>`<font style="color:rgb(51, 51, 51);">和</font>`<font style="color:rgb(51, 51, 51);">NVM_SYMLINK</font>`<font style="color:rgb(51, 51, 51);">默认是</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">安装好后自动配置，如果没有的话就手动去加一下。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846127448-a6e3d8e0-f026-43a3-8401-72c4007792f2.png)

<font style="color:rgb(51, 51, 51);">5.点击新建。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846128500-24128476-9076-496f-afa1-c6600cb457ac.png)

<font style="color:rgb(51, 51, 51);">6.在变量名中分别输入我们的</font>`<font style="color:rgb(51, 51, 51);">NVM_HOME</font>`<font style="color:rgb(51, 51, 51);">和</font>`<font style="color:rgb(51, 51, 51);">NVM_SYMLINK</font>`<font style="color:rgb(51, 51, 51);">。</font>`<font style="color:rgb(51, 51, 51);">NVM_HOME</font>`<font style="color:rgb(51, 51, 51);">对应的值是我们</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的安装路径</font>`<font style="color:rgb(51, 51, 51);">NVM_SYMLINK</font>`<font style="color:rgb(51, 51, 51);">对应的值是我们</font>`<font style="color:rgb(51, 51, 51);">nodejs</font>`<font style="color:rgb(51, 51, 51);">的安装路径。系统变量和用户变量的操作是一样的。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846128360-9c2d5808-ae96-4044-afa5-72db287d7ba5.png)

<font style="color:rgb(51, 51, 51);">7.找到我们用户变量的中变量名为</font>`<font style="color:rgb(51, 51, 51);">Path</font>`<font style="color:rgb(51, 51, 51);">的变量，选中之后点击编辑。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846129172-fb936f73-5956-4433-8960-f7dbab45dabf.png)

<font style="color:rgb(51, 51, 51);">8.点击新建在我们右侧输入框中分别输入我们</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">和</font>`<font style="color:rgb(51, 51, 51);">nodejs</font>`<font style="color:rgb(51, 51, 51);">的安装路径。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846131402-f71dab89-a8f1-4dd8-ac1b-506ada12f9f8.png)<font style="color:rgb(51, 51, 51);">  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846133753-96d5e04c-4784-4979-a99d-a033fc2c8604.png)

<font style="color:rgb(51, 51, 51);">9.找到我们</font>`<font style="color:rgb(51, 51, 51);">nvm</font>`<font style="color:rgb(51, 51, 51);">的安装路径，点击文件夹中的</font>`<font style="color:rgb(51, 51, 51);">settings.txt</font>`<font style="color:rgb(51, 51, 51);">的文件。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846134358-aa22ed0b-172c-40cc-b31a-81711c97b2a3.png)

<font style="color:rgb(51, 51, 51);">10.打开</font>`<font style="color:rgb(51, 51, 51);">settings.text</font>`<font style="color:rgb(51, 51, 51);">文档后，加入以下两行，保存后退出。</font>

```plain
node_mirror: https://npmmirror.com/mirrors/node/
npm_mirror: https://npmmirror.com/mirrors/npm/
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846135941-59043577-61cd-42aa-86e1-aecc115e1edd.png)

<font style="color:rgb(51, 51, 51);">11.找到</font>`<font style="color:rgb(51, 51, 51);">nodejs</font>`<font style="color:rgb(51, 51, 51);">的安装路径，分别新建</font>`<font style="color:rgb(51, 51, 51);">node_cache</font>`<font style="color:rgb(51, 51, 51);">和</font>`<font style="color:rgb(51, 51, 51);">node_global</font>`<font style="color:rgb(51, 51, 51);">两个文件夹。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846138992-579c1cc3-453c-49c6-a80c-323941c679e1.png)

<font style="color:rgb(51, 51, 51);">12.创建完两个文件夹后，打开</font>`<font style="color:rgb(51, 51, 51);">cmd</font>`<font style="color:rgb(51, 51, 51);">窗口后输入分别以下命令（两个路径分别是两个文件夹的路径）。</font>

```plain
npm config set prefix "node_global的文件路径"
npm config set cache "node_cache的文件路径"
```

### <font style="color:rgb(51, 51, 51);">四.nvm的使用</font>
<font style="color:rgb(51, 51, 51);">1.打开</font>`<font style="color:rgb(51, 51, 51);">cmd</font>`<font style="color:rgb(51, 51, 51);">窗口输入</font>`<font style="color:rgb(51, 51, 51);">nvm list available</font>`<font style="color:rgb(51, 51, 51);">就可以看到我们能够安装的</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">版本。（没有要安装的版本话就去</font>`<font style="color:rgb(51, 51, 51);">node</font>`官网<font style="color:rgb(51, 51, 51);">去找到</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">的版本号）。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846142626-240175d0-bf3d-4b6b-adad-b7c193be98a8.png)

<font style="color:rgb(51, 51, 51);">2.输入</font>`<font style="color:rgb(51, 51, 51);">nvm install "node对应的版本号"</font>`<font style="color:rgb(51, 51, 51);">就可以下载</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846150078-78fb39c3-b388-419d-b5cc-4f5142d9bcb7.png)

<font style="color:rgb(51, 51, 51);">3.查看我们本地的</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">,可以看到我们刚刚下载的</font><font style="color:rgb(51, 51, 51);">node</font><font style="color:rgb(51, 51, 51);">版本号已经有了。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846161017-d955a6c6-e421-47d0-981e-64d9c63e6282.png)

<font style="color:rgb(51, 51, 51);">4.</font>`<font style="color:rgb(51, 51, 51);">*</font>`<font style="color:rgb(51, 51, 51);">表示我们当前使用的</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">版本，现在我们来使用刚刚安装的</font>`<font style="color:rgb(51, 51, 51);">20.16.0</font>`<font style="color:rgb(51, 51, 51);">。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846161091-bce074e2-7ce2-4373-9648-3d5f79950e99.png)

<font style="color:rgb(51, 51, 51);">5.我们在验证一下</font>`<font style="color:rgb(51, 51, 51);">node</font>`<font style="color:rgb(51, 51, 51);">是否安装和使用完成。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733846166806-87a012ac-fa51-40ff-a8d2-a3acfb5c0b1c.png)

### <font style="color:rgb(51, 51, 51);">五.</font><font style="color:rgb(51, 51, 51);">nvm的常用命令</font>
```plain
nvm list available           //查看查看可安装的node版本
nvm version                  //安装指定版本的 Node.js、简写 nvm -v
nvm install <version>        //安装指定版本的 Node.js。
nvm use <version>            //切换使用指定版本的 Node.js。
nvm list                     //列出已安装的所有 Node.js 版本、简写 nvm ls
nvm alias <name> <version>   //创建一个别名以便更方便地引用特定的 Node.js 版本。
nvm uninstall <version>      //卸载指定的 Node.js 版本。
nvm current                  //显示当前正在使用的 Node.js 版本。
nvm use default              //切换到默认的 Node.js 版本（由 nvm alias 命令设置的别名）。
nvm exec <version> <command> //在指定版本的 Node.js 环境中执行特定的命令。
```

### <font style="color:rgb(51, 51, 51);">六.设置npm源</font>
```javascript
// 设置npm源
npm config set registry https://registry.npmmirror.com/

// 查看npm 源
npm config get registry

```


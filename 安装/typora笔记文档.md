### 一、安装typora
下载zip，并解压

### 二、创建github仓库
##### 2.1 创建github仓库
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434334420-de74a91a-9f74-4262-a5e8-0ca36dfe724f.png)

##### 2.2 拉去仓库到本地
复制地址

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434388523-48caae0a-bfd5-4dbc-92ae-619092ba3b24.png)

输入 git clone xxx 拉取仓库

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434422436-4ac7014f-e62a-48ec-98c7-98c33a891001.png)

##### 3.3 添加文件后 提交并推送到仓库
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434496512-c5b222b8-339a-4162-b9be-7521f0e0e5cf.png)

```shell
# 把所有文件添加到git仓库中
git add .
# 提交文件
git commit -m "提交信息"
# 推送到远程
git push

# 第一次会让你配置全局 git 邮箱 和 git user, 配置完成之后再推送
git config --global user.email "17090315867@163.com"
git comfig --global user.name "shizq"

# 推送成功！
```

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434754085-09d870cb-0468-4fe8-bd72-b01b54ab526d.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434791279-ec7ff392-d571-4870-b95b-2356a739f51a.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434798397-388eff35-cd4a-4d04-abea-73fd7ea12591.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434827019-bde0b9bc-6934-45b8-a858-29fa0c252bc9.png)

### 三、配置图片
现在在文档中添加的图片只会保存在本地（如图），要想实现图片多端同步就要配置图床

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736434920937-61136352-5bb8-465d-a55e-750c15e36617.png)

**图床：**

所谓图床，就是将图片上传到服务器，并得到一个外网能够访问到URL地址；市面上有很多款公共的图床，比如：https://sm.ms/ ；这些图床都是可以正常使用的，但是存在一个致命的问题，我们可以轻松上传图片，但是没办法去销毁这些图片；所以，构建属于自己的个性化图床还是很有必要的；

自定义免费图床，**<font style="color:rgb(37, 132, 181);">github</font>**、**<font style="color:rgb(37, 132, 181);">码云</font>**和**<font style="color:rgb(37, 132, 181);">七牛云</font>**都是不错的选择，配置好之后，不仅能自由的上传，还能自由删除不想要、不想公开的图片；虽然七牛搭建图床有免费10G空间，但是配置过程需要已经备案域名，这一点就给很多朋友带了很大的障碍，所以在这里暂时就不介绍七牛云图床了；今天就详细的讲解一下如何基于github配置完全免费的图床

##### 3.1 github免费图床
###### 注册并登录github账号。 [https://github.com/](https://github.com/) 
###### 创建图床项目
这里说的项目，也可以理解为目录，就是图片最终存放的位置；

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736435285283-1b4617d3-86f2-4e2a-9f14-7e4b622181a4.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736435799979-9b2e5919-5bfb-4b0b-a955-d2224d6a79fe.png)

###### 配置token
进入账号的 Settings

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736435354386-16f726b2-7107-4768-b419-b44a6d019e96.png)

###### 选择开发者配置
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736435408351-40efb512-d027-4a60-98c1-32f47816c2a4.png)

###### 创建一个Token
###### ![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736435561169-55c0b7c1-24a8-4b0b-a954-08f9206a4b15.png)
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736435634598-d25925af-1f1f-4627-8202-f0be0adabe1f.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436078902-36e35d2f-dc5c-48f1-bd29-41d32eb72ba1.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436141644-13da1284-a325-461e-86ba-d21c19a8f5cb.png)

记住Token，**<font style="color:rgb(37, 132, 181);">请务必保存好此Token，关闭之后，将不会再显示，也无法查看</font>**

**<font style="color:rgb(37, 132, 181);">到此，github图床的准备工作已经完成了，请保存好项目名称和Token，下一步将使用到；</font>**

**<font style="color:rgb(37, 132, 181);"></font>**

##### 3.2 PicGo
一款功能非常强大的图床的工具，支持`<font style="color:rgb(30, 107, 184);">SM.MS</font>`、`<font style="color:rgb(30, 107, 184);">腾讯COS</font>`、`<font style="color:rgb(30, 107, 184);">GitHub图床</font>`、`<font style="color:rgb(30, 107, 184);">七牛云图床</font>`、`<font style="color:rgb(30, 107, 184);">Imgur图床</font>`、`<font style="color:rgb(30, 107, 184);">阿里云OSS</font>`、`<font style="color:rgb(30, 107, 184);">又拍云图床</font>`、`<font style="color:rgb(30, 107, 184);">gitee</font>`等多种图床平台；

PicGo默认使用的是SMMS图床：https://sm.ms/ ；如果你没有配置好上面的github图床或者gitee图床，且图片也并不那么重要且可以公开，也可以直接使用默认的SMMS图床来管理图片即可。

下载地址：

> [https://github.com/Molunerfinn/PicGo/releases](https://github.com/Molunerfinn/PicGo/releases)
>

特点：

要说特点，PicGO**<font style="color:rgb(37, 132, 181);">最大的特点是，可以和Typora结合使用</font>**，配置好关联之后，Typora写文章时，如果需要穿插图片，只需要将图片复制粘贴到Typora的编辑区域，就自动通过PicGo上传到指定图床，得到外网能访问的URL并展示；如果没有网络的情况下，也能通过PicGo暂存在本地，等有网络的时候，再次进行上传即可。关联配置后面会专门讲解

###### 下载
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436438480-2186590e-a18e-44bb-8a43-75af9573e10b.png)

###### 安装
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436525645-dffd680b-aa64-4f73-a02d-9d0f21811156.png)

###### 运行配置
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436581569-ee7fdf75-5b0b-474b-b894-83344f6109e5.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436791910-be5f79a3-a075-45a5-83b2-3a551b560644.png)

确认并设置为默认图床即可

###### 测试上传
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736436950218-9610f8e2-b6d7-49fe-b9e1-29ebd036ac2e.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736437836851-924e9960-6dc3-42dd-8bd3-8468672c09ce.png)

###### 解决github访问慢的问题
默认情况下，在国内访问github是非常慢的，有时候甚至会出现根本访问不到的情况，最后导致图片无法上传到github图床，我们可以借助一款免费的CDN加速器：

> [https://cdn.jsdelivr.net](https://cdn.jsdelivr.net)
>

<font style="color:black;">可以完美的解决github访问不稳定的问题，这个免费CDN已经使用半年，这期间访问的github图床几乎很少出现问题，非常方便，配置也很简单：</font>

<font style="color:black;">只需要将github的域名换成https://cdn.jsdelivr.net/gh，如下实例：</font>

<font style="color:black;">加速前地址：https://github.com/CG-RECT/Typora_notes_images</font>

<font style="color:black;">加速后的地址：https://cdn.jsdelivr.net/gh/CG-RECT/Typora_notes_images</font>

**<font style="color:rgb(37, 132, 181);">PicGo配置github图床加速</font>**

将加速后的访问地址填在自定义域名即可。

**<font style="color:#DF2A3F;">或者设置代理</font>**：

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736437916604-75b53a4f-c2ee-414f-92f2-ce30d7c8848b.png)

##### 3.3 typora关联PicGo
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736438104591-68619338-0436-4a1a-a030-907f97aec9bd.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736438076689-e72cf387-1c5f-4092-bd6c-2c1f4ef1f602.png)

如上图所示，说明已经关联成功了。

### 四、整体测试
经过上面的一系列配置之后，就可以使用Markdown开始写文章了；图片这些，截图粘贴之后，就自动通过PicGo上传到了远端图床，小效果如下：

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736439215646-e8c948ad-d8da-46ad-a72c-27dfbad0a3d0.png)

至此，我们就可以专心写文章了，再也不用花精力去处理图片，排版这些琐碎、耗时的工作。


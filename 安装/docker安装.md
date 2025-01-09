# 【Docker】Windows11操作系统下安装、使用Docker保姆级教程_docker windo11
<font style="color:rgb(51, 51, 51);">Docker</font><font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">支持开发人员使用简单的命令访问这些本机</font>[<font style="color:rgb(51, 51, 51);">容器化</font>](https://edu.csdn.net/cloud/sd_summit?utm_source=glcblog&spm=1001.2101.3001.7020)<font style="color:rgb(51, 51, 51);">功能，并通过节省工作量的应用程序编程接口 (API) 自动执行。 与 LXC 相比，Docker 提供了以下功能：</font>

+ <font style="color:rgb(51, 51, 51);">增强的无缝容器</font>`<font style="color:rgb(51, 51, 51);">可移植性</font>`<font style="color:rgb(51, 51, 51);">：虽然 LXC 容器通常引用特定于机器的配置，但 Docker 容器无需修改即可在任何桌面、数据中心和云环境中运行。</font>
+ <font style="color:rgb(51, 51, 51);">更轻巧且</font>`<font style="color:rgb(51, 51, 51);">更细粒度的更新</font>`<font style="color:rgb(51, 51, 51);">：通过使用 LXC，可以在单个容器中组合多个进程。 这样就可以构建持续运行的应用，即使为了更新或修复而关闭某个部分也不例外。</font>
+ `<font style="color:rgb(51, 51, 51);">自动化容器创建</font>`<font style="color:rgb(51, 51, 51);">：Docker 可以基于应用源代码自动构建容器。</font>
+ `<font style="color:rgb(51, 51, 51);">容器版本控制</font>`<font style="color:rgb(51, 51, 51);">：Docker 可以跟踪容器映像的版本，回滚到先前的版本，以及跟踪版本的构建者和构建方式。 它甚至可以</font>`<font style="color:rgb(51, 51, 51);">只上传现有版本和新版本之间的增量</font>`<font style="color:rgb(51, 51, 51);">。</font>
+ `<font style="color:rgb(51, 51, 51);">容器复用</font>`<font style="color:rgb(51, 51, 51);">：现有容器可用作</font>`<font style="color:rgb(51, 51, 51);">基本映像</font>`<font style="color:rgb(51, 51, 51);">（本质上类似于用于构建新容器的模板）。</font>
+ `<font style="color:rgb(51, 51, 51);">共享容器库</font>`<font style="color:rgb(51, 51, 51);">：开发人员可以访问包含数千个用户贡献容器的</font>`<font style="color:rgb(51, 51, 51);">开源注册表</font>`<font style="color:rgb(51, 51, 51);">。</font>

_<font style="color:rgb(51, 51, 51);">如今，Docker 容器化也适用于 Microsoft</font>__<font style="color:rgb(51, 51, 51);"> </font>__<font style="color:rgb(51, 51, 51);">Windows</font>__<font style="color:rgb(51, 51, 51);"> </font>__<font style="color:rgb(51, 51, 51);">和 Apple MacOS。 开发人员可以在任何操作系统上运行 Docker 容器，大多数领先的云提供商（包括 Amazon Web Services (AWS)、Microsoft Azure 和 IBM Cloud）都提供了一些专用服务，这些服务可帮助开发人员构建、部署和运行使用 Docker 进行容器化的应用。</font>_

---

_**<font style="color:rgb(51, 51, 51);">在初步认识了解了</font>**_`_**<font style="color:rgb(51, 51, 51);">Docker</font>**_`_**<font style="color:rgb(51, 51, 51);">后，下面正式进入</font>**_`_**<font style="color:rgb(51, 51, 51);">Docker</font>**_`_**<font style="color:rgb(51, 51, 51);">使用环节！</font>**_

#### <font style="color:rgb(51, 51, 51);">一、进入Docker官网</font>
<font style="color:rgb(51, 51, 51);">首先先到Docker官网下载最新官方Docker for Windows链接：</font>

[https://docs.docker.com/desktop/setup/install/windows-install/](https://docs.docker.com/desktop/setup/install/windows-install/)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072454858-d14686d7-bfff-41b7-a907-2823e1b4c11f.png)

---

#### <font style="color:rgb(51, 51, 51);">二、启动Microsoft Hyper-V</font>
_<font style="color:rgb(51, 51, 51);">在电脑上打开“控制面板”->“程序”-> “启动或关闭Windows功能”。</font>_

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455150-7d009a31-919f-49c0-a4e5-4aaceaf74d1c.png)

+ <font style="color:rgb(51, 51, 51);">勾选</font>`<font style="color:rgb(51, 51, 51);">Hype-V</font>`<font style="color:rgb(51, 51, 51);">功能</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072454942-d87662d6-31cf-4ce1-8def-86fe7ba8eb75.png)

+ <font style="color:rgb(51, 51, 51);">并勾选如下内容:</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072454795-7ee8f475-9916-40b9-9cb1-9ff894bdd1a7.png)

---

#### <font style="color:rgb(51, 51, 51);">三、安装Docker</font>
##### 3.1 更改安装路径
如果需要更改安装路径的话，用win11的cmd输入命令

```plain
"Docker Desktop Installer.exe" install --installation-dir="D:\devtools\docker"
```



![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072884166-898e2a81-5608-4219-9679-67de5ec374bf.png)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734073032037-280973f5-b1b6-4648-99c4-01fbfe4f0c90.png)

##### <font style="color:rgb(51, 51, 51);">3.2 在Windows上安装Docker桌面版</font>
+ <font style="color:rgb(51, 51, 51);">双击程序，如下：  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072454932-80da1c1a-f8f8-412b-8a40-95be1f8e4c9a.png)

---

+ <font style="color:rgb(51, 51, 51);">点击OK，确定安装</font>`<font style="color:rgb(51, 51, 51);">WSL</font>`

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455374-18e1cbce-c00a-489c-8df0-f47914794390.png)

+ <font style="color:rgb(51, 51, 51);">等待安装完毕！</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455428-03ac3348-49f9-4989-8a41-911928e00841.png)

---

+ <font style="color:rgb(51, 51, 51);">安装完毕后，点击</font>`<font style="color:rgb(51, 51, 51);">Close and restart</font>`

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455597-c59f9b52-282b-4c15-85b7-16a44ac9934e.png)

---

+ <font style="color:rgb(51, 51, 51);">电脑重启后，点击</font>`<font style="color:rgb(51, 51, 51);">Docker</font>`<font style="color:rgb(51, 51, 51);">程序会看到如下界面</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455762-482e7bd0-4e3b-4681-9a8a-462a8b7b9e68.png)

---

+ <font style="color:rgb(51, 51, 51);">默认勾选，点击</font>`<font style="color:rgb(51, 51, 51);">Finish</font>`<font style="color:rgb(51, 51, 51);">即可完成  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455820-4c1a460d-4c0f-4811-8a93-e0f6d52b3c9c.png)
+ <font style="color:rgb(51, 51, 51);">等待启动</font>`<font style="color:rgb(51, 51, 51);">Docker</font>`<font style="color:rgb(51, 51, 51);">引擎</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072455935-8235f68d-56c8-4f4e-885e-b568c455ee8f.png)

+ <font style="color:rgb(51, 51, 51);">报错如下：</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456177-fbd23533-9ec2-4f85-8132-d49565685e3f.png)

+ <font style="color:rgb(51, 51, 51);">重新更新一下</font>`<font style="color:rgb(51, 51, 51);">wsl</font>`<font style="color:rgb(51, 51, 51);">版本，如下命令</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456148-ca352ef8-150f-419a-a083-7d14d35b72bf.png)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456614-751a1746-782c-4002-9df0-7e8607efd624.png)

+ <font style="color:rgb(51, 51, 51);">报错如下：点击</font>`<font style="color:rgb(51, 51, 51);">restart</font>`<font style="color:rgb(51, 51, 51);">重启即可。  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456605-1b3a215f-3538-4070-a6fa-e17f9c913ca4.png)
+ <font style="color:rgb(51, 51, 51);">现在程序正常启动并稳定啦</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456649-1207d88e-cec3-45b9-8195-be3c872607ad.png)

---

#### <font style="color:rgb(51, 51, 51);">四、玩转Docker</font>
+ <font style="color:rgb(51, 51, 51);">命令行输入如下命令</font>

```plain
docker --version
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456598-a6b858ba-9d40-46aa-9ef0-2e43c88746c3.png)

_<font style="color:rgb(51, 51, 51);">至此就可以在windows上开始Docker之路啦!</font>_

#### <font style="color:rgb(51, 51, 51);">五、运行Hello-world</font>
+ <font style="color:rgb(51, 51, 51);">运行Hello-world，使用如下命令：</font>

```plain
docker pull hello-world
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072456709-e66171ed-b94c-4765-b49c-de3be67e9d8c.png)

+ <font style="color:rgb(51, 51, 51);">查看是否拉取成功？</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457031-bcc7fc0d-caf1-408f-b12f-6c71ea8d2725.png)

_<font style="color:rgb(51, 51, 51);">显示Hello-world镜像确实存在！</font>_

+ <font style="color:rgb(51, 51, 51);">查看可视化容器镜像，显示如下：</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457191-73c113d7-0b91-4cf6-b922-86cbfea28ba0.png)

_<font style="color:rgb(51, 51, 51);">至此拉取Hello-world成功！</font>_

---

#### <font style="color:rgb(51, 51, 51);">六、配置阿里云镜像加速</font>
常见的docker国内镜像：

```plain
常见的Docker Hub国内镜像地址
配置aliyun的镜像：crpi-qdl3zr1kdzwfo3bd.cn-hangzhou.personal.cr.aliyuncs.com
wo94aijingxiang
#配置登录： docker login --username=szq184019435 crpi-qdl3zr1kdzwfo3bd.cn-hangzhou.personal.cr.aliyuncs.com
wo94aijingxiang

阿里云镜像：registry.cn-hangzhou.aliyuncs.com
网易云镜像：hub-mirror.c.163.com
DaoCloud镜像：daocloud.io
七牛云镜像：reg.qiniu.com
Docker中国区官方镜像 https://registry.docker-cn.com
ustc  https://docker.mirrors.ustc.edu.cn
中国科技大学  https://docker.mirrors.ustc.edu.cn
阿里云容器 服务  https://cr.console.aliyun.com/
腾讯云  https://mirror.ccs.tencentyun.com

```

+ <font style="color:rgb(51, 51, 51);">刚才的</font>`<font style="color:rgb(51, 51, 51);">pull</font>`<font style="color:rgb(51, 51, 51);">操作比较慢，接下来需要配置一下镜像代理，便于更快速的拉取资源！</font>
+ <font style="color:rgb(51, 51, 51);">登录阿里云官网：</font>
+ [**https://cr.console.aliyun.com/cn-hangzhou/instances/mirrors**](https://cr.console.aliyun.com/cn-hangzhou/instances/mirrors)<font style="color:rgb(51, 51, 51);">(需要账号登录)</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734074147862-26c0ba2e-18ec-4e6d-a00e-5c08b796d034.png)

_<font style="color:rgb(51, 51, 51);">地址是免费的，每个人都有。</font>_

---

+ <font style="color:rgb(51, 51, 51);">将如下代码添加到</font>`<font style="color:rgb(51, 51, 51);">Docker</font>`<font style="color:rgb(51, 51, 51);">的设置中</font>

```plain
{
  "registry-mirrors": [
    "https://73oa5swq.mirror.aliyuncs.com",
    "https://mirror.ccs.tencentyun.com"]
}

或者配置：
[
		"https://docker.registry.cyou",
		"https://docker-cf.registry.cyou",
		"https://dockercf.jsdelivr.fyi",
		"https://docker.jsdelivr.fyi",
		"https://dockertest.jsdelivr.fyi",
		"https://mirror.aliyuncs.com",
		"https://dockerproxy.com",
		"https://mirror.baidubce.com",
		"https://docker.m.daocloud.io",
		"https://docker.nju.edu.cn",
		"https://docker.mirrors.sjtug.sjtu.edu.cn",
		"https://docker.mirrors.ustc.edu.cn",
		"https://mirror.iscas.ac.cn",
		"https://docker.rainbond.cc"
		]
```

+ <font style="color:rgb(51, 51, 51);">进入设置的页面</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457421-b6be6c89-344e-4dae-8b55-03a74eda8680.png)

---

+ <font style="color:rgb(51, 51, 51);">添加如下：</font>

<font style="color:rgb(51, 51, 51);">点击</font>`<font style="color:rgb(51, 51, 51);">Apply andr esatrt</font>`<font style="color:rgb(51, 51, 51);"> 运用并重启即可</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457346-5324f83c-9c13-4a17-85ff-8bab4c4cd32c.png)

_<font style="color:rgb(51, 51, 51);">至此配置阿里云镜像加速完毕！</font>_

---

#### <font style="color:rgb(51, 51, 51);">七、容器常用命令</font>
##### <font style="color:rgb(51, 51, 51);">查看版本</font>
```plain
docker --version
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457605-be857f7b-2c43-434e-aa0f-a81857527c14.png)

---

##### <font style="color:rgb(51, 51, 51);">获取镜像</font>
<font style="color:rgb(51, 51, 51);">如果我们本地没有</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">mysql</font>`<font style="color:rgb(51, 51, 51);">镜像，我们可以使用</font>`<font style="color:rgb(51, 51, 51);">docker pull</font>`<font style="color:rgb(51, 51, 51);">命令来载入</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">mysql</font>`<font style="color:rgb(51, 51, 51);">镜像：</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457771-6a023ae6-f878-4d93-ae20-aee0629a853a.png)

---

##### <font style="color:rgb(51, 51, 51);">查看镜像</font>
```plain
docker images
```

<font style="color:rgb(51, 51, 51);">查看所有镜像源：  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072457969-7928cad8-443b-4414-91f0-bd64e70ecb28.png)

---

##### <font style="color:rgb(51, 51, 51);">启动容器</font>
<font style="color:rgb(51, 51, 51);">以下命令使用</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">mysql</font>`<font style="color:rgb(51, 51, 51);">镜像启动一个容器，参数为以命令行模式进入该容器：</font>

```plain
docker run -it mysql /bin/bash
```

_<font style="color:rgb(51, 51, 51);">输入</font>_`_<font style="color:rgb(51, 51, 51);">exit</font>_`_<font style="color:rgb(51, 51, 51);">容器停止运行</font>_

<font style="color:rgb(51, 51, 51);">所以，更常用的是这种后台启动的方式:</font>

```plain
docker run -itd mysql /bin/bash
```

---

_<font style="color:rgb(51, 51, 51);">注意每</font>_`_<font style="color:rgb(51, 51, 51);">run</font>_`_<font style="color:rgb(51, 51, 51);">一个就创建一个容器！</font>_

<font style="color:rgb(51, 51, 51);">参数说明：</font>

+ `<font style="color:rgb(51, 51, 51);">-i</font>`<font style="color:rgb(51, 51, 51);">: 交互式操作。</font>
+ `<font style="color:rgb(51, 51, 51);">-t</font>`<font style="color:rgb(51, 51, 51);">: 终端。</font>
+ `<font style="color:rgb(51, 51, 51);">mysql</font>`<font style="color:rgb(51, 51, 51);">: mysql镜像。</font>
+ `<font style="color:rgb(51, 51, 51);">/bin/bash</font>`<font style="color:rgb(51, 51, 51);">：放在镜像名后的是命令，这里我们希望有个交互式</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">Shell</font>`<font style="color:rgb(51, 51, 51);">，因此用的是</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">/bin/bash</font>`<font style="color:rgb(51, 51, 51);">。  
</font><font style="color:rgb(51, 51, 51);">要退出终端，直接输入</font><font style="color:rgb(51, 51, 51);"> </font>`<font style="color:rgb(51, 51, 51);">exit</font>`

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072458208-59963b8a-c549-4eac-bb18-8fa9a8ee7c00.png)

---

+ <font style="color:rgb(51, 51, 51);">指定配置信息运行容器</font>

<font style="color:rgb(51, 51, 51);">运行容器，一般是指定容器内的端口和容器的名字(不能与之前的名字重复)</font>

`<font style="color:rgb(51, 51, 51);">--expose</font>`<font style="color:rgb(51, 51, 51);">:编辑容器内的端口</font>

`<font style="color:rgb(51, 51, 51);">--name</font>`<font style="color:rgb(51, 51, 51);">:编辑容器的名字</font>

<font style="color:rgb(51, 51, 51);">最后的</font>`<font style="color:rgb(51, 51, 51);">my-golang-app</font>`<font style="color:rgb(51, 51, 51);"> </font><font style="color:rgb(51, 51, 51);">为镜像源</font>

```plain
docker run --expose 3888/tcp --name mycontainer-15 my-golang-app
```

---

##### <font style="color:rgb(51, 51, 51);">删除容器</font>
```plain
docker rm -f 容器ID
```

<font style="color:rgb(51, 51, 51);">运行结果如下:</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072458334-610cdce2-3f97-4ab5-9144-f7371dd1767d.png)

---

##### <font style="color:rgb(51, 51, 51);">批量删除</font>
```plain
docker rm -f 容器ID1 容器ID2 容器ID……
```

<font style="color:rgb(51, 51, 51);">运行结果如下：</font>

```plain
[root@localhost docker]# docker rm -f 31094a8a38df d6e155d5c175 a49250b3790b 87a94ee8c07f ffd24d4aaeca b2b6aeaa9073 ca4c7c1ff87c ccce1fb65649 07efbc1eb5ad
31094a8a38df
d6e155d5c175
a49250b3790b
87a94ee8c07f
ffd24d4aaeca
b2b6aeaa9073
ca4c7c1ff87c
ccce1fb65649
07efbc1eb5ad
[root@localhost docker]# docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

---

##### <font style="color:rgb(51, 51, 51);">查看容器</font>
<font style="color:rgb(51, 51, 51);">常用命令如下：</font>

```plain
docker ps -a
```

<font style="color:rgb(51, 51, 51);">运行结果如下:  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072458392-3be23ac1-b003-426e-a40d-4ece692bcd90.png)

```plain
docker ps -q
```

<font style="color:rgb(51, 51, 51);">运行结果如下:  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072458772-bfd4a624-9a73-4ace-81e7-98a468856107.png)

`<font style="color:rgb(51, 51, 51);">ps</font>`<font style="color:rgb(51, 51, 51);">：列出正在运行的容器。</font>

<font style="color:rgb(51, 51, 51);">参数说明：</font>

+ `<font style="color:rgb(51, 51, 51);">-a</font>`<font style="color:rgb(51, 51, 51);">：列出所有容器（包括停止的容器）。</font>
+ `<font style="color:rgb(51, 51, 51);">-q</font>`<font style="color:rgb(51, 51, 51);">：仅显示容器ID。</font>
+ `<font style="color:rgb(51, 51, 51);">-f</font>`<font style="color:rgb(51, 51, 51);">：根据过滤器条件过滤输出。</font>
+ `<font style="color:rgb(51, 51, 51);">"name=CONTAINER_NAME"</font>`<font style="color:rgb(51, 51, 51);">：过滤器条件，匹配指定名称的容器。</font>

---

##### <font style="color:rgb(51, 51, 51);">暂停容器</font>
```plain
docker pause 容器ID
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072458710-066e24c4-c0b1-49d5-9833-02862617a84b.png)

_<font style="color:rgb(51, 51, 51);">暂停容器的运行，但是容器并没有停止。</font>_

---

```plain
docker unpause 容器ID
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072458983-bc05adbc-b3a4-4df5-a29f-07ff1ff52f11.png)

_<font style="color:rgb(51, 51, 51);">恢复容器的暂停。</font>_

---

##### <font style="color:rgb(51, 51, 51);">停止容器</font>
```plain
docker stop 容器ID
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072459081-05624b3d-6708-432f-b348-77073715dbbd.png)

_<font style="color:rgb(51, 51, 51);">使用此命令会停止容器的运行,如果想不停止运行，可以使用暂停的命令。</font>_

---

##### <font style="color:rgb(51, 51, 51);">重启容器</font>
```plain
docker restart 容器ID
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072459124-3de2e8f1-a566-43c0-b051-cfa779c73630.png)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734072459325-b0b88a74-894a-4d87-973f-9adbda6245c0.png)



<font style="color:rgb(51, 51, 51);">  
</font>


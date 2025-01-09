## <font style="color:rgb(51, 51, 51);">1、在Windows上安装Maven</font>
### <font style="color:rgb(51, 51, 51);">1.1 检查</font><font style="color:rgb(51, 51, 51);">JDK安装</font>
<font style="color:rgb(51, 51, 51);">在安装</font><font style="color:rgb(51, 51, 51);">Maven</font><font style="color:rgb(51, 51, 51);">之前，首先要确认已经正确安装了JDK。Maven可以运行在JDK1.4及以上的版本上。打开Windows的命令行，运行如下的命令来检查Java安装情况：</font>

```vbnet
C:\Users\panjunbiao>echo %Java_Home%

C:\Users\panjunbiao>java -version
```

**<font style="color:rgb(51, 51, 51);">执行结果：</font>**

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733845441037-f04894a9-eaae-4f5f-b76d-5b08d376847a.png)

<font style="color:rgb(51, 51, 51);">上述命令首先检查环境变量Java_Home是否指向了正确的JDK目录，接着运行Java命令。如果Windows无法执行Java命令，或者无法找到Java_Home环境变量，就需要检查Java是否安装了，或者环境变量是否设置正确。</font>

### <font style="color:rgb(51, 51, 51);">1.2 下载Maven</font>
<font style="color:rgb(51, 51, 51);">Maven的下载页面：</font>[https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi)

<font style="color:rgb(51, 51, 51);">如下图，点击并下载Maven的压缩文件。</font>

![](https://cdn.nlark.com/yuque/0/2024/jpeg/22229609/1733845386892-4651e850-f110-4b36-98df-492a5b0c8ea9.jpeg)

<font style="color:rgb(51, 51, 51);">下载完成后，将安装文件解压到指定的目录中。解压后的目录结构如下：</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733845507221-0d27e0fe-d71e-45e2-bfb8-9534c7ce0d7d.png)

### <font style="color:rgb(51, 51, 51);">1.3 设置环境变量</font>
<font style="color:rgb(51, 51, 51);">接着需要设置环境变量，将Maven安装配置到操作系统环境中。打开系统属性面板（在桌面上右键“我的电脑” → “属性”），单击高级系统设置。</font>

#### <font style="color:rgb(51, 51, 51);">1.3.1 设置Maven_Home环境变量</font>
**<font style="color:rgb(51, 51, 51);">（1）新建系统变量</font>**

<font style="color:rgb(51, 51, 51);">变量名：Maven_Home</font>

<font style="color:rgb(51, 51, 51);">变量值：D:\</font><font style="color:rgb(51, 51, 51);">apache</font><font style="color:rgb(51, 51, 51);">-maven-3.6.3</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733845575955-66dba303-d753-46fd-aae6-38fb4bdfeb50.png)

**<font style="color:rgb(51, 51, 51);">（2）修改Path变量值</font>**

<font style="color:rgb(51, 51, 51);">在Path变量值后面加上：;%Maven_Home%\bin;</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733845608287-2a23746f-a63b-4fc5-9008-a253123a4532.png)

#### <font style="color:rgb(51, 51, 51);">1.3.2 设置MAVEN_OPTS环境变量</font>
<font style="color:rgb(51, 51, 51);">变量名：MAVEN_OPTS</font>

<font style="color:rgb(51, 51, 51);">变量值：-Xms128m -Xmx512m</font>

<font style="color:rgb(51, 51, 51);">设置MAVEN_OPTS环境变量不是必须的，但建议设置。因为Java默认的最大可用内存往往不能够满足Maven运行的需要，比如在项目较大时，使用Maven生成项目站点需要占用大量的内存，如果没有该配置，则很容易得到java.lang.OutOfMemeoryError。因此，一开始就配置该变量是推荐的做法。</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733845667807-fa3f879d-c87f-43c5-a9da-29651dd2d058.png)

### <font style="color:rgb(51, 51, 51);">1.4 检查Maven安装</font>
<font style="color:rgb(51, 51, 51);">配置完成环境变量后，新增打开一个新的cmd窗口（这里强调新的窗口是因为新的环境变量配置需要新的cmd窗口才能生效），运行如下命令检查Maven的安装情况：</font>

```vbnet
C:\Users\panjunbiao>echo %Maven_Home%

C:\Users\panjunbiao>mvn -v
```

**<font style="color:rgb(51, 51, 51);">执行结果：</font>**

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733845785233-c2085de6-3db6-428b-8e35-266c6f5d90f9.png)

<font style="color:rgb(51, 51, 51);">第一条命令echo %Maven_Home%用来检查环境变量Maven_Home是否指向了正确的Maven安装目录；而mvn -v是Maven的执行命令，以检查Windows系统是否能够找到正确的mvn执行脚本。</font>

## <font style="color:rgb(51, 51, 51);">2、Maven的配置</font>
### <font style="color:rgb(51, 51, 51);">2.1 生成.m2文件夹</font>
<font style="color:rgb(51, 51, 51);">在cmd窗口中执行如下命令：</font>

```perl
mvn help:system
```

<font style="color:rgb(51, 51, 51);">先运行一条简单的命令：mvn help:system。该命令会打印出所有的Java系统属性和环境变量，这些信息对我们日常的变成工作很有帮助。该命令的目的是让Maven执行一个正在的任务。我们可以从命令行输出看到Maven会下载\maven-help-plugin，包括pom文件和jar文件。这些文件都被下载到了Maven本地仓库中。</font>

<font style="color:rgb(51, 51, 51);">现在.m2文件夹就生成了，在用户目录下可以找到.m2文件夹，如：C:\Users\panjunbiao\.m2</font>

<font style="color:rgb(51, 51, 51);">默认情况下，该文件夹下放置了Maven本地仓库（C:\Users\panjunbiao\.m2\repository），所有的Maven构件都被存储到该仓库中，可以方便重用。可以到C:\Users\panjunbiao\.m2\repository\org\apache\maven\</font><font style="color:rgb(51, 51, 51);">plugins</font><font style="color:rgb(51, 51, 51);">\maven-help-plugin目录下找到刚刚下载的maven-help-plugin的pom文件和jar文件。</font>

### <font style="color:rgb(51, 51, 51);">2.2 配置用户范围的settings.xml文件</font>
<font style="color:rgb(51, 51, 51);">默认情况下，.m2文件夹下除了repository仓库之外就没有其他目录和文件了，不过大多数Maven用户需要复制安装目录下的D:\apache-maven-3.6.3\conf\settings.xml文件到.m2文件夹下C:\Users\panjunbiao\.m2\settings.xml。这是一条最佳实践。</font>

<font style="color:rgb(51, 51, 51);">Maven用户可以选择配置安装目录下的\conf\settings.xml文件或者.m2文件夹下的settings.xml文件。前者是全局范围的，整台机器上的所有用户都会直接受到该配置的影响，而后者是用户范围的，只有当前用户才会受到该配置的影响（推荐）。</font>

### <font style="color:rgb(51, 51, 51);">2.3 配置Maven本地仓库</font>
<font style="color:rgb(51, 51, 51);">打开.m2文件夹下的settings.xml文件，添加如下配置：</font>

```html
<!-- 设置本地仓库位置 -->
<localRepository>D:\develop\apache-maven-3.6.3\repo</localRepository>
```

<font style="color:rgb(51, 51, 51);">这样Maven本地仓库就不用在C盘下了。</font>

### <font style="color:rgb(51, 51, 51);">2.4 配置中央仓库的镜像（改用：阿里云中央仓库镜像）</font>
<font style="color:rgb(51, 51, 51);">有时我们通过Maven去下载相关的依赖包时，会发现下载的速度非常慢，而有时又下载不了，没有响应。为什么会这么慢呢，原因是Maven默认连接的远程仓库是国外的（http://repo1.maven.org/maven2/）。为了提升下载速度，只要把Maven默认的镜像改换成国内的就行了，如阿里云的中央仓库镜像。</font>

<font style="color:rgb(51, 51, 51);">在settings.xml文件下的<mirrors>节点中，添加如下配置：</font>

```html
<!-- 配置中央仓库的镜像（改用：阿里云中央仓库镜像）-->
<mirror>        
  <id>alimaven</id>
  <name>aliyun-maven</name>
  <mirrorOf>central</mirrorOf>
  <url>http://maven.aliyun.com/nexus/content/groups/public</url>
</mirror>
```


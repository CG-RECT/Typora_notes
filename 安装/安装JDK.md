## <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">一、JDK简介</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK（Java Development Kit，</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">Java开发工具</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">包）是用于开发Java应用程序的工具集。它包括了一系列开发工具和库，用于编写、编译、调试和运行Java程序。JDK是Java开发者必须安装的</font>[<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">软件</font>](https://marketing.csdn.net/p/3127db09a98e0723b83b2914d9256174?pId=2782&utm_source=glcblog&spm=1001.2101.3001.7020)<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">包。</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK通常包括以下主要组件：</font>

1. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">Java编译器 (javac)</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：用于将Java源代码编译成字节码 (.class 文件)。</font>
2. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">Java运行时环境 (JRE)</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：包括Java虚拟机 (JVM) 和标准类库，用于运行Java应用程序。JRE是JDK的一部分。</font>
3. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">Java解释器/加载器 (java)</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：用于解释和运行字节码。</font>
4. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">标准类库</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：一系列标准类库，提供常用的功能，例如数据结构、数学运算、输入输出、网络编程等。</font>
5. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">开发工具</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：如调试器 (jdb)、文档生成器 (javadoc)、归档工具 (jar) 等。</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK 使开发者能够从编写代码到将其打包为可分发的应用程序。每个JDK版本都会引入新的功能、</font>[<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">性能</font>](https://marketing.csdn.net/p/3127db09a98e0723b83b2914d9256174?pId=2782&utm_source=glcblog&spm=1001.2101.3001.7020)<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">改进和安全更新，因此开发者通常会选择适合其项目需求的版本进行开发。</font>

## <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">二、JDK版本</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">截至2024年，</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">Oracle</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">的Java Development Kit (JDK) 主要有以下几个长期支持 (LTS) 版本被认为是稳定版本：</font>

1. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK 8</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：发布于2014年3月，广泛使用并得到长期支持。</font>
2. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK 11</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：发布于2018年9月，是另一个LTS版本，广泛用于生产环境。</font>
3. **<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK 17</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">：发布于2021年9月，是最新的LTS版本，得到长期支持。</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">非LTS版本也会在各自发布周期内得到支持，但生命周期较短。例如，JDK 9、JDK 10、JDK 12-16 等都属于非LTS版本，通常支持六个月。对于生产环境，建议选择LTS版本以获得长期的安全更新和稳定性支持。</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">那多说无益我们来开始安装</font>

## <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">三、JDK安装（</font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">JDK 17)</font>**
### <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">1、JDK下载</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">（下载地址）</font>[https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)

```plain
https://www.oracle.com/java/technologies/downloads/
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844293874-d05e6cde-ef3b-4778-9829-bb7ff9d752a5.png)

### <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">2、JDK安装</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">我们得到安装包，双击！</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844400682-34210b7c-2e87-4b1f-808e-4abc160df9dd.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;"></font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">下一步</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844428226-8e727fdd-114c-4ef7-82d7-ceaf67df9606.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;"></font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">选择</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">更改</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">或者直接</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">下一步</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844448298-824ca873-5b15-4d93-9d1e-8609b02a0137.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;"></font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">更改路径</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844462687-0908f7c6-82c9-4b81-893e-fead47fef199.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;"></font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">继续</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">下一步</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844471699-67b5d510-4fab-4eb6-bb24-3fb04b8d0eb7.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">出现这个页面就安装成功了！</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844480537-8cfe7426-b946-4406-a65c-cd4fce927699.png)

## <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">四、配置环境变量</font>
### <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">1、环境变量简介</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">环境变量是一个动态命名值，它能够影响系统运行过程中的行为。这些变量可以用于存储系统配置和其他信息，以便操作系统和应用程序可以访问这些信息。环境变量通常用于配置应用程序的运行环境，简化命令行操作，以及设置系统路径等。</font>

### <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">2、配置JAVA_HOME</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">此电脑鼠标右击点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">属性</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844493670-a7631656-b415-40f5-a75a-08f3d100f175.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">高级系统设置</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844504452-d22bebea-1fdc-471b-b645-baff9b9ae832.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">环境变量</font>

v![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844525770-fc94f150-5790-42bc-883f-ae515fe994b3.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">在</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">系统变量</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">新建</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844536224-0dba7132-5900-44d8-8af8-985c2a4e6049.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">变量名：JAVA_HOME</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">变量值：上面自己的安装路径</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">如果没改，默认为：</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">C:\Program Files\Java\jdk-17</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844546150-01a594b6-8b81-4eec-a38c-69a34adc23aa.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">填写完毕之后点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">确定</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">回到环境变量</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">系统变量点击Path，然后点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">编辑</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844554387-44a7c401-a5ca-4086-a75f-b53fe4f2a48d.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">进入页面点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">新建</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844561616-af01ba20-b754-451e-9b14-10f47511cd7b.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">将JAVA_HOME加到Path里</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;"></font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;"> </font>**<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">%JAVA_HOME%\bin</font>**

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">然后点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">确认</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844569676-bf483b24-3abe-4d86-8cf1-0186fcc97565.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">回到环境变量点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">确认</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844579287-ad31d9dc-0dbd-4db8-8961-45920e4be860.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">回到系统属性继续点击</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">确认</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844599769-96b95cdd-725d-4935-bf7a-031595a14593.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">这样我们的JDK环境变量就配置好了，那我们该如何检验呢？</font>

## <font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">五、查看是否安装成功</font>
<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">点击WIN+R(WIN键是键盘上画着窗口图标键）</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">输入cmd</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844613600-22420596-e647-41a1-a943-ec5021fa5b32.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">回车之后我们进入到命令窗口里</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">输入：java -version 回车  
</font>![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844626632-8b86d5b6-a8e7-45b1-b60d-1e886ebb62de.png)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1733844635049-0c7f9701-c1a3-4f58-a88c-79c98f50487c.png)

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">如果显示出JDK版本那我们就大功告成啦！</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">ps</font><font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">:如果不成功，就重启电脑，有的系统编辑环境变量后只有重启后才会生效！</font>

<font style="color:rgb(51, 51, 51);background-color:#FFFFFF;">  
</font>


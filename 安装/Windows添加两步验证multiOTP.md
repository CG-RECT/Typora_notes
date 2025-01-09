# <font style="color:rgb(25, 27, 31);">缘起</font>
<font style="color:rgb(25, 27, 31);">前几天朋友用来做</font>[<font style="color:rgb(25, 27, 31);">winnas</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=winnas&zhida_source=entity)<font style="color:rgb(25, 27, 31);">的电脑远程桌面被爆破中了</font>[<font style="color:rgb(25, 27, 31);">勒索病毒</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=%E5%8B%92%E7%B4%A2%E7%97%85%E6%AF%92&zhida_source=entity)<font style="color:rgb(25, 27, 31);">，还好是在调试阶段，损失不大。是因为ipv4公网ip加上设置的密码太弱了，被人轻松搞掉。想起我也有一台常开的本地windows，虽说有点防护，但还是感觉不到位，前车之鉴后车之师，我决定给windows装个两步验证，让自己安心。</font>

# <font style="color:rgb(25, 27, 31);">折腾</font>
<font style="color:rgb(25, 27, 31);">两步验证方面可用的软件挺多的，不过好多都收费，找了个开源的项目来试试。软件叫multiotp，在全球最大同行交流网站能找到该项目。首先进到</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">https://download.multiotp.net/credential-provider/</font>`<font style="color:rgb(25, 27, 31);">这个网站，如图示，拉到最下面，下载最新的软件，下载好解压出来备用。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405159564-04370352-f2f0-4944-b282-a55d00d8ab28.png)

<font style="color:rgb(25, 27, 31);">一般来说如果你电脑的</font>[<font style="color:rgb(25, 27, 31);">运行库</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=%E8%BF%90%E8%A1%8C%E5%BA%93&zhida_source=entity)<font style="color:rgb(25, 27, 31);">齐全的话直接进到解压后的目录下，双击“multiOTPCredentialProviderInstaller”文件安装即可，如果安装程序报错的话先到</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">https://support.microsoft.com/zh-cn/help/2977003/the-latest-supported-visual-c-downloads</font>`<font style="color:rgb(25, 27, 31);">微软官方下载安装Microsoft Visual C++运行库，具体操作如图示，根据自己系统下载对应程序，下载好后直接双击安装即可。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405183349-27c54a16-0ecf-4efe-b8c8-416ba18837e9.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405500691-595decd9-a5eb-4fd5-9bfe-f0592a5f3027.png)

<font style="color:rgb(25, 27, 31);">装好运行库，运行安装程序一般来说就不会报错了。如图示，第一个页面直接点击“next”下一步；页面勾选同意协议然后再点“next”下一步；一个页面“multiOTp Login Title”这个框是输入登录标题啥的，可改可不改，我改了似乎没啥效果，勾选上“No</font><font style="color:rgb(25, 27, 31);"> </font>[<font style="color:rgb(25, 27, 31);">remote server</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=remote+server&zhida_source=entity)<font style="color:rgb(25, 27, 31);">, local multioTP only”然后点“next”下一步。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405522531-449b4e95-cc5a-42ec-89df-c9da78f237fa.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405571615-66a8ab86-2e2a-408a-aa36-02f9a6ee49ba.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405635292-dbcfeb5e-39a3-4f0a-a90d-6341952c1dea.png)

<font style="color:rgb(25, 27, 31);">新的页面保持默认选项，直接点“next”下一步。新的页面的设置就比较重要了，这里是要选择哪种登录方式需要两步验证，一般来说我们都选“only remote</font><font style="color:rgb(25, 27, 31);"> </font>[<font style="color:rgb(25, 27, 31);">远程登录</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=%E8%BF%9C%E7%A8%8B%E7%99%BB%E5%BD%95&zhida_source=entity)<font style="color:rgb(25, 27, 31);">需要验证就行了。点“next”下一步，来到最后一个页面，直接点“install”开始安装程序，很快就装好了，最后点“finish”结束安装。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405670064-abf7ee5a-4662-4fef-aa49-dcd0554954f6.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405693046-d33e85a5-f80c-4f49-8a33-41682a917665.png)



![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405722690-40382118-05e9-4f1f-88af-99ae1b792252.png)

<font style="color:rgb(25, 27, 31);">安装完程序后，还需要进行些设置，我们来到multiotp的</font>[<font style="color:rgb(25, 27, 31);">安装目录</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=%E5%AE%89%E8%A3%85%E7%9B%AE%E5%BD%95&zhida_source=entity)<font style="color:rgb(25, 27, 31);">，一般来说是在</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">C:\Program Files\multiOTP</font>`<font style="color:rgb(25, 27, 31);">目录下。以管理员权限打开</font>[<font style="color:rgb(25, 27, 31);">命令提示符</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6&zhida_source=entity)<font style="color:rgb(25, 27, 31);">，输入命令</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">cd C:\Program Files\multiOTP</font>`<font style="color:rgb(25, 27, 31);">回车，进到multiotp的安装目录；然后输入</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">multiotp.exe -fastcreatenopin Administrator</font>`<font style="color:rgb(25, 27, 31);">命令回车，其中Administrator是你要设置两步验证的用户名。输入完这段代码后就能在multiotp的安装目录看到新建的users文件夹。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405797726-f1efbbcd-7aea-4d54-91dc-ca9f350a8ff8.png)



![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736405939641-444b4475-d409-445f-80dd-b3d45666e101.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736406051956-dc91cb13-8985-480d-84b9-78574d241920.png)

<font style="color:rgb(25, 27, 31);">打开两步验证后，我们还需要将其添加到两步验证器上，有两种方法，手机的话比较方便的是生成一个二维码扫描添加，操作如图示，在命令行中输入</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">multiotp.exe -qrcode Administrator Administrator.png</font>`<font style="color:rgb(25, 27, 31);">回车后就能看到在安装目录生成了一个Administrator.png二维码图片，用手机扫描二维码就可以将其添加到两步</font>[<font style="color:rgb(25, 27, 31);">验证器</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=2&q=%E9%AA%8C%E8%AF%81%E5%99%A8&zhida_source=entity)<font style="color:rgb(25, 27, 31);">上了。另一种就是生成url来方便添加到电脑上，在命令行输入</font>`<font style="color:rgb(25, 27, 31);background-color:rgb(248, 248, 250);">multiotp.exe -urllink Administrator</font>`<font style="color:rgb(25, 27, 31);">回车后就会出现个链接，将“secret=xxxxx&”=和&之间的密钥复制出来。粘贴进</font>[<font style="color:rgb(25, 27, 31);">身份验证器</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=1&q=%E8%BA%AB%E4%BB%BD%E9%AA%8C%E8%AF%81%E5%99%A8&zhida_source=entity)<font style="color:rgb(25, 27, 31);">就可以了。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736406149749-628e3c46-3117-4dd9-b0a4-f7e0f8acbe85.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736406165225-21f03cb8-36f5-444b-9c2b-bf830de0c432.png)



<font style="color:rgb(25, 27, 31);">现在来试试效果，重连</font>[<font style="color:rgb(25, 27, 31);">远程桌面</font>](https://zhida.zhihu.com/search?content_id=240317375&content_type=Article&match_order=2&q=%E8%BF%9C%E7%A8%8B%E6%A1%8C%E9%9D%A2&zhida_source=entity)<font style="color:rgb(25, 27, 31);">，duang~两步验证就出现了。</font>

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736406327261-c44814d4-bd2b-4af5-afde-57606f88e4ea.png)

如果想替换登录头像的话，要替换 C:\Program Files\multiOTP 文件夹下的 loginLogo.bmp 图片就可以

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736406484158-7cccc05a-fe73-451b-8a4a-3fcdbeb3211d.png)

# <font style="color:rgb(25, 27, 31);">总结</font>
<font style="color:rgb(25, 27, 31);">互联网水太深还是要保护好自己啊，身边遇到的第一例被勒索的，还好损失不大，设置一个强密码是关键，加一个两步验证就更加放心了。</font>


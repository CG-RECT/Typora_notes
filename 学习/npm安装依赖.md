npm 



npm安装并显示详细信息

npm install --verbose 

#### 配置代理
<font style="color:rgb(51, 51, 51);"></font>

<font style="color:rgb(44, 44, 54);">如果你位于公司网络或需要通过代理访问互联网，不正确的代理配置会导致 </font>`<font style="color:rgb(44, 44, 54);">npm install</font>`<font style="color:rgb(44, 44, 54);"> 变得非常缓慢甚至失败。</font>

#### <font style="color:rgb(44, 44, 54);">解决方案：</font>
+ <font style="color:rgb(44, 44, 54);">正确配置 HTTP 和 HTTPS 代理：</font>

```shell

npm config set proxy http://proxy-server:port
npm config set https-proxy http://proxy-server:port
```

+ <font style="color:rgb(44, 44, 54);">确保代理服务器本身没有性能问题或者过载。</font>

<font style="color:rgb(51, 51, 51);"></font>


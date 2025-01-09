### 一、去GitHub地址下载源码
##### 1.1 github下载地址： [https://github.com/vuejs/vue-devtools](https://github.com/vuejs/vue-devtools)
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736408397674-893f403b-2785-47ee-9d57-04466a1eeee0.png)

如下图，下载最新版 6.6.4

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736408457465-d1ab8f35-4759-4a91-9c05-f31a7af82ef1.png)

##### 1.2 下载之后解压到本地文件夹
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736408753108-e1384535-e800-444b-907e-7d8baa9dd20e.png)

### 二、安装并编译
##### 2.1 npm安装 
在 vue.js-devtools 根目录下 （devtools-v6-6.6.4）只行 cmd 命令，下载依赖

npm install

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736409074792-7a0ae3d1-4b90-4981-8896-825870b28c06.png)

##### 2.2 进行编译
执行cmd命令，npm run build

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736410357763-f6fa4c89-a0ea-488c-bc0d-772a78eb3918.png)

##### 2.3 修改 mainfest.json 文件
找到 shells\chrome\manifest.json 文件，将 persistent 改为 true

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736410578012-ee5ae80c-9ea7-4b17-ba3a-7abc47f3027a.png)

### 三、安装到chrome插件中
##### 3.1 在chrome浏览器中 扩展程序界面 cheome://extensions 右上方【开发者模式】打开
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736410669653-79648525-8e4b-4e4c-b68a-f43d1f6d6cb8.png)

##### 3.2 加载已解压的扩展程序
![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736410746389-a1f2ec1f-e8ce-4a6d-8bdf-970b001b9a30.png)

安装完成

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736410802545-fcc299c1-0b8e-4fd6-9806-ad5b45ad93e8.png)

### 四、应用商店安装
也可以在谷歌应用商店搜索并安装插件

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736410903025-71323205-a1a4-4a29-9d66-e59119b09e92.png)


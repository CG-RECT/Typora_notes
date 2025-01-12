Docker官网：[https://www.docker.com/](https://www.docker.com/)

Docker官方文档：[https://docs.docker.com/desktop/setup/install/windows-install/](https://docs.docker.com/desktop/setup/install/windows-install/)

# 一、Docker概述
### 1.1 Docker为什么会出现？
一款产品： 开发-上线 两套环境！ 应用环境，应用配置！

开发 ... 运维， 问题：我在我的电脑上可以运行！版本更新，导致服务不可用！对于运维来说，考验就十分大？

开发即运维!

环境配置十分的麻烦，每一个机器都要部署环境(集群Redis、ES、Hadoop...)！费时费力。

发布一个项目 jar + (Redis MySQL jdk ES) ，项目能不能带上环境安装打包!

之前在服务器配置一个应用的环境 Redis MySQL jdk ES Hadoop，配置很麻烦，不能够跨平台。

Windows,最后发布到Linux！

传统：开发jar  运维来做！

现在：开发打包部署上线，一套流程做完！



java -- apk --发布（应用商店） --- 张三使用apk -- 安装即可用！

java -- jar(环境) -- 打包项目带上环境(镜像) --- （Docker仓库：商店） -- 下载我们发布的镜像-- 直接运行即可！



Docker给以上的问题，提出了解决方案！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734531562368-42c7e070-df7f-43e0-9b98-80dd05838c35.png)

Docker的思想就来自于集装箱！

JRE -- 多个应用（端口冲突）--原来都是交叉的

隔离：Docker核心思想！打包装箱！每个箱子都是互相隔离的

水果 生化武器

Docker通过隔离机制，可以将服务器利用到极致！



本质：所有的技术都是因为出现了一些问题，我们需要去解决，采取学习！

### 1.2 Docker的历史
2010年，几个搞IT的年轻人，就在美国成立了一家公司`dotCloud`

做一些pass的云计算服务！LXC有关的容器技术！

他们将自己的技术-（容器化技术）命名就是 Docker ！

Docker刚刚诞生的时候，没有引起行业的注意！dotCloud，就活不下去！

`开源`- 开放源代码！

2013年，Docker开源！

Docker越来越多的人发现了docker的优点！火了，Docker每个月都会更新一个版本！

2014年4月9日，Docker1.0发布！

Docker为什么这么火？十分的轻巧！

在容器技术出来之前，我们都是使用的虚拟机技术！

虚拟机：在windows中装一个Vmware，通过这个软甲你我们可以虚拟出来一台或者多台电脑！笨重！

虚拟机也是属于虚拟化技术，Docker容器技术，也是一种虚拟化技术！

```plain
vm - linux centos原生镜像（一个电脑）隔离，需要开启多个虚拟机！ 几个G 几分钟
docker，隔离，镜像（最核心的环境 4m + jdk + mysql）十分的小巧，运行镜像就可以了！小巧！ 几个M KB 秒级启动！
```

到现在，所有开发人员都必须要会Docker！

### 1.3 聊聊Docker
官网：[https://www.docker.com/](https://www.docker.com/)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734532560032-d873f475-f69b-4dbb-b68e-91dbdfc6ec7a.png)

文档地址：[https://docs.docker.com/](https://docs.docker.com/) Docker的文档是超级详细的！

仓库地址：[https://hub.docker.com/](https://hub.docker.com/)  

### 1.4 Docker能干嘛
---

:::info
虚拟机技术

:::

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734533127708-daf2ddc2-f6b4-4f3a-8d60-f94f9ab0b6e8.png)

虚拟技术缺点：

1.资源占用十分多

2.冗余步骤多

3.启动很慢！

:::info
容器化技术

:::

<font style="color:#DF2A3F;">容器化技术不是模拟的一个完整的操作系统</font>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734533267883-7acbf07c-5e0a-4120-a9df-c43646569180.png)

比较 Docker 和 虚拟机技术的不同：

+ 传统虚拟机，虚拟出一条硬件，运行一个完整的操作系统，然后在这个系统上安装和运行软甲你
+ 容器内的樱花用直接运行在 宿主机的内容，容器时没有自己的内核的，也没有秀妮我们的硬件，所以就轻便了
+ 每个容器间是互相隔离，每个容器内都有有一个属于自己的文件系统，互不影响。

:::info
DevOps （开发、运维）

:::

 **应用更快速的交付和部署**

传统： 一堆帮助文档，安装程序

Docker：打包镜像发布测试，一键运行

**更编辑的升级和扩容**

使用了Docker之后，我们部署应用就和搭积木一样！

SpringBoot 1.5   Redis 5 tomcat8 升级

项目打包为一个镜像，扩展 服务器A 服务器B

**更简单的系统运维**

在容器化之后，我们的开开发，测试环境都是高度一致的。

**更高效的计算资源利用：**

Docker是 内核级别的虚拟化，可以在一个物理机上运行很多的容器实例！服务器的性能可以被压榨到极致！

# 二、Docker安装
参考： [Docker安装](https://www.yuque.com/shizq-mwj08/gb7q9e/tzfvxp449sr58ebv#mainContentTitle)

**镜像（image）：**

docker镜像就好比是一个模板，可以通过这个模板来创建容器服务，tomcat镜像===>run===>tomcat01容器（提供服务器）

**容器（container）：**

Docker利用容器技术，独立运行一个或一个组应用，通过镜像来创建的。

启动、停止、删除，基本命令！

目前就可以把这个容器理解为一个简易的Linux系统

**仓库（repository）：**

仓库就是存放镜像的地方！

仓库分为公有仓库和私有仓库！

Docker Hub（默认是国外的）

阿里云... 都有容器服务器（配置镜像加速！）

### 2.1 安装Docker
> 环境准备
>

1.需要会一点点的Linux的基础

2.CentOS7

3.我们使用Xshell连接远程服务器进行操作！

> 环境查看
>

```plain
#系统内核时 3.10 以上的
uname -a
Linux ZQ 5.15.167.4-microsoft-standard-WSL2 #1 SMP Tue Nov 5 00:21:55 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux
```

```plain
# 系统版本 cat /etc/os-release
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734534563695-fd5cfba5-f741-4ae3-b4eb-6398fe3a1976.png)

> 安装
>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734534805345-73a8d035-a64e-4611-b401-9c6a17d578a3.png)

帮助文档：

```shell
# 1.卸载旧的版本
sudo dnf remove docker \
  docker-client \
  docker-client-latest \
  docker-common \
  docker-latest \
  docker-latest-logrotate \
  docker-logrotate \
  docker-engine
# 2.需要的安装包
sudo dnf -y install dnf-plugins-core
# 3.设置镜像的仓库 （默认是国外的，推荐用国内的）
sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

# 更新 软件包索引

# 4.安装docker  docker-ce 社区   ee 企业版
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
# 5.启动docker
sudo systemctl enable --now docker
# 6.使用docker version 检测是否安装成功

# 7.hello-world
sudo docker run hello-world

# 8.查看一下下载的这个 hello-world镜像是否在
docker images

```

> 了解卸载：
>

```shell
#1. 下载依赖
sudo dnf remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
# 2.删除资源
rm -rf /var/lib/docker/

# /var/lib/docker/  docker的默认工作路径！

```

### 2.2 镜像加速
##### 1.登录阿里云，找到镜像容器服务
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734535759640-00a21f96-df74-44c2-baec-64c4218765e5.png)

##### 2.找到镜像加速地址
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734535830519-268a52a3-a37d-47ce-b297-7d47c5c0b6bd.png)

##### 3.配置使用
```shell
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://73oa5swq.mirror.aliyuncs.com"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
```

### 2.3 回顾HelloWorld流程
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734536103392-d6b222b7-b0e5-4453-b450-8b77ea39a289.png)

### 2.4 底层原理
**docker是怎么工作的？**

Docker是一个Client-Server 结构的系统，Docker的守护进程在主机上，通过Socket从客户端访问！

DockerServer 接收到 Docker-Client 的指令，就会执行这个命令！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734536395586-b843ab8c-ee69-49d6-9259-d34b86f3e412.png)

**Docker为什么比 VM 快**

1.Docker 有着比虚拟机更少的抽线层

2.docker利用的是宿主机的内核， vm 需要是Guest OS。

所以说，新建一个容器的时候，docker不需要像虚拟机一样重新加载一个操作系统内核，避免引导，虚拟机时加载Guest OS，分钟级别的，而Docker是利用 宿主机的操作系统，省略了这个复杂的过程，秒级！



之后学习完毕所有的命令，再回过头来看这段理论，就会很清晰！



# 三、Docker命令
### 3.1 帮助命令
```shell
docker version  #版本信息
docker info   # 显示docker的系统信息，包括经镜像和容器的数量
docker 命令 --help   # 万能命令
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734536971169-9167a6c3-d745-48ce-b909-2e8c72b1c31b.png)

### 3.2 镜像命令
```shell
docker images 查看所有镜像的命令
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
redis        latest    b5e874b32a79   2 months ago    117MB
mysql        5.7       5107333e08a8   12 months ago   501MB

# 解释
repository 	镜像的仓库源
tag					镜像的标签
image id 		镜像的id
created 		镜像的创建时间
size 				镜像的大小

# 可选项
-a, -all    		# 列出所有镜像
-q, -quiet			# 列出镜像的id


```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734537140430-25319108-0554-45e7-a196-fccdd1a56ed9.png)

##### 3.2.1 docker search 搜索镜像
```shell
docker search 搜索镜像

docker search mysql
NAME                   DESCRIPTION                                      STARS     OFFICIAL
mysql                  MySQL is a widely used, open-source relation…   15542     [OK]
bitnami/mysql          Bitnami container image for MySQL                122

# 可选项, 通过收藏来过滤
--filter=STARS=3000   搜索出来的镜像就是stars大于3000的

```

##### 3.2.2 docker pull 下载镜像
```shell
# 下载镜像 docker pull 镜像名[:tag]
docker pull mysql
Using default tag: latest 	# 如果不写 tag，默认就是 latest
iaosfoiasfuioL: pull complete # 分层下载 docker image的核心 联合文件系统
Digest: sha256:daishdiouahifhasioas  #签名
Status: 
docker.io/library/myhsql:latest # 真实地址

# 等价于它
docker pull mysql
docker pull docker.io/library/myhsql:latest

# 指定版本下载
docker pull mysql:5.7

```

##### 3.2.3 镜像删除
```shell
docker rmi -f 镜像id 		# 删除指定的镜像
docker rmi -f 镜像id 镜像id 镜像id  # 删除多个镜像
docker rmi -f $(docker images -aq) # 删除全部的镜像
```

### 3.3 容器命令
说明：我们有了镜像才可以创建容器，linux，下载一个 centos 镜像来测试学习。

```shell
docker pull centos
```

新建容器并启动

```shell
docker run [可选参数] image

# 参数说明
--name="Name" 	容器名字 tomcat01   tomcat02, 用来区分容器
-d 							后台运行方式
-it 						使用交互方式运行，进入容器查看内容
-p 							指定容器的端口 -p 8080:8080
  -p ip:主机端口:容器端口
  -p 主机端口:容器端口 （常用）
-P（大写P） 			随机指定端口


# 测试 启动并进入容器
docker run -it centos /bin/bash

[root@7836f3aaef21 /]# ls  	# 查看容器内的centos，基础版本，很多命令还不是完善的
bin  dev  etc  home  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

exit 	# 退出

```

##### 3.3.1 列出所有的运行的容器
```shell
# docker ps 命令
    # 列出当前正在运行的容器
-a  # 列出当前正在运行的容器 + 带出历史运行过的容器
-n=? 		# 显示最近创建的容器
-q 			# 只显示容器的编号

C:\Users\17090>docker ps -a
CONTAINER ID   IMAGE          COMMAND                   CREATED         STATUS                          PORTS     NAMES
7836f3aaef21   centos         "/bin/bash"               2 minutes ago   Exited (0) About a minute ago             elastic_clarke
93e8c61a5c7a   mysql:5.7      "docker-entrypoint.s…"   3 days ago      Exited (0) 24 hours ago                   mysql5.7
c46bb66ab7bf   redis:latest   "docker-entrypoint.s…"   4 days ago      Exited (0) 24 hours ago                   lucid_heyrovsky

```

##### 3.3.2 删除容器
```shell
exit  	# 直接容器停止并退出
Ctrl + P + Q  # 容器不停止退出

docker rm 容器id  		# 删除指定的容器（不能删除正在运行的容器，如果渝澳强制删除 rm -f）
docker rm -f $(docker ps -aq) 	# 删除所有的容器
docker ps -a -q|xargs docker rm   # 删除所有的容器

```

##### 3.3.3 启动和停止容器的操作
```shell
docker start 容器id 	# 启动容器
docker restart 容器id	# 重启容器
docker stop 容器id		# 停止当前正在运行的容器
docker kill 容器id		# 前置停止当前容器
```

### 3.4 常用其他命令
##### 3.4.1 后台启动容器
```shell
# 命令 docker run -d 镜像名
docker run -d centos

# 问题docker ps,发现 centos 停止了

# 常见的坑， docker 容器使用后台运行，就必须要有一个前台进程，docker发现没有应用，就会自动停止
# nginx，容器启动后，发现自己没有提供服务，就会立刻停止，就是没有程序了

```

##### 3.4.2 查看日志
```shell
docker logs -f -t --tail 容器， 没有日志

# 自己编写一段shell脚本
zq@ZQ:~$ docker run -d centos /bin/sh -c "while true;do echo zhiq;sleep 1;done"

zq@ZQ:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS     NAMES
fa303b3a994f   centos    "/bin/sh -c 'while t…"   2 seconds ago   Up 2 seconds             cranky_nightingale

# 显示日志
-tf 		# 显示日志
--tail number  	# 要显示日志的条数

zq@ZQ:~$ docker logs -tf --tail 10 fa303b3a994f

```

##### 3.4.3 查看容器中的进程信息
```shell
# docker top 容器id
zq@ZQ:~$ docker top fa303b3a994f
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                774                 754                 0                   16:37               ?                   00:00:00            /bin/sh -c while true;do echo zhiq;sleep 1;done
root                1022                774                 0                   16:41               ?                   00:00:00            /usr/bin/coreutils --coreutils-prog-shebang=sleep /usr/bin/sleep 1
```

##### 3.4.4 镜像元数据
```shell
# 命令
docker inspect 容器id

# 测试
zq@ZQ:~$ docker inspect fa303b3a994f
[
    {
        "Id": "fa303b3a994f21b81096f2b8c3633676803d4d7fb1c66e5a5e9bd47a917f9e5f",
        "Created": "2024-12-18T16:37:21.483885149Z",
        "Path": "/bin/sh",
        "Args": [
            "-c",
            "while true;do echo zhiq;sleep 1;done"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 774,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2024-12-18T16:37:21.598426202Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:5d0da3dc976460b72c77d94c8a1ad043720b0416bfc16c52c45d4847e53fadb6",
        "ResolvConfPath": "/var/lib/docker/containers/fa303b3a994f21b81096f2b8c3633676803d4d7fb1c66e5a5e9bd47a917f9e5f/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/fa303b3a994f21b81096f2b8c3633676803d4d7fb1c66e5a5e9bd47a917f9e5f/hostname",
        "HostsPath": "/var/lib/docker/containers/fa303b3a994f21b81096f2b8c3633676803d4d7fb1c66e5a5e9bd47a917f9e5f/hosts",
        "LogPath": "/var/lib/docker/containers/fa303b3a994f21b81096f2b8c3633676803d4d7fb1c66e5a5e9bd47a917f9e5f/fa303b3a994f21b81096f2b8c3633676803d4d7fb1c66e5a5e9bd47a917f9e5f-json.log",
        "Name": "/cranky_nightingale",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "bridge",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                30,
                120
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": [],
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware",
                "/sys/devices/virtual/powercap"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/554d578944fbc3a0df6dd411e53ad1a19e7274698fd573b5e896103b9d208168-init/diff:/var/lib/docker/overlay2/55f848c988d2eaf96e20b8ad52cb5bbdb155f122442686ffb6634ae790fe59fd/diff",
                "MergedDir": "/var/lib/docker/overlay2/554d578944fbc3a0df6dd411e53ad1a19e7274698fd573b5e896103b9d208168/merged",
                "UpperDir": "/var/lib/docker/overlay2/554d578944fbc3a0df6dd411e53ad1a19e7274698fd573b5e896103b9d208168/diff",
                "WorkDir": "/var/lib/docker/overlay2/554d578944fbc3a0df6dd411e53ad1a19e7274698fd573b5e896103b9d208168/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "fa303b3a994f",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/sh",
                "-c",
                "while true;do echo zhiq;sleep 1;done"
            ],
            "Image": "centos",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "desktop.docker.io/wsl-distro": "Ubuntu",
                "org.label-schema.build-date": "20210915",
                "org.label-schema.license": "GPLv2",
                "org.label-schema.name": "CentOS Base Image",
                "org.label-schema.schema-version": "1.0",
                "org.label-schema.vendor": "CentOS"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "1312f362da004b8a4d63931804078f5685e07da0bb45e5b7f754e6ab54437bf8",
            "SandboxKey": "/var/run/docker/netns/1312f362da00",
            "Ports": {},
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "cc290737cb8551fd73e1e9af74ee942c87f4743da0f3424e133fc2f34cbab40f",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null,
                    "NetworkID": "28ca7f2e5f4d6136d3410b3394698e61682fab2504dbc924eea83479bdc1055d",
                    "EndpointID": "cc290737cb8551fd73e1e9af74ee942c87f4743da0f3424e133fc2f34cbab40f",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "DNSNames": null
                }
            }
        }
    }
]
```

##### 3.4.5 进入当前正在运行的容器
```shell
# 我们通常容器都是使用后台方式运行的，需要进入容器，修改一些配置

# 命令
docker exec -it 容器id bashShell

# 测试
zq@ZQ:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS     NAMES
fa303b3a994f   centos    "/bin/sh -c 'while t…"   8 minutes ago   Up 8 minutes             cranky_nightingale
zq@ZQ:~$
zq@ZQ:~$
zq@ZQ:~$ docker exec -it fa303b3a994f /bin/bash
[root@fa303b3a994f /]# ls
bin  dev  etc  home  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
[root@fa303b3a994f /]#

# 方式二
docker attach 容器id
# 测试
docker attach fa303b3a994f
正在执行当前的代码。。


# docker exec				# 进入容器后开启一个新的终端，可以在里面操作（c常用）
# docker attach 		# 进入容器正在执行的终端，不会启动新的进程
```

##### 3.4.6 从容器内拷贝到主机上
```shell

docker cp 容器id:容器内路径 	目的主机路径

zq@ZQ:/home$ docker ps
CONTAINER ID   IMAGE     COMMAND       CREATED         STATUS         PORTS     NAMES
54a05a65a860   centos    "/bin/bash"   2 minutes ago   Up 2 minutes             intelligent_mestorf
# 进入 docker 容器内部
zq@ZQ:/home$ docker attach 54a05a65a860
[root@54a05a65a860 /]# cd /home/
[root@54a05a65a860 home]# ls
# 创建一个文件
[root@54a05a65a860 home]# touch bb.java
[root@54a05a65a860 home]# ls
bb.java
[root@54a05a65a860 home]# ll
bash: ll: command not found
# 退出容器
[root@54a05a65a860 home]# exit
exit
zq@ZQ:/home$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
zq@ZQ:/home$ docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS                        PORTS     NAMES
54a05a65a860   centos         "/bin/bash"              3 minutes ago    Exited (127) 11 seconds ago             intelligent_mestorf
34e6c4b09e28   centos         "/bin/sh -C 'while t…"   19 minutes ago   Exited (127) 19 minutes ago             intelligent_yonath
2bee38428989   centos         "/bin/bash"              23 minutes ago   Exited (0) 18 minutes ago               unruffled_cray
7836f3aaef21   centos         "/bin/bash"              40 minutes ago   Exited (0) 38 minutes ago               elastic_clarke
93e8c61a5c7a   mysql:5.7      "docker-entrypoint.s…"   3 days ago       Exited (0) 24 hours ago                 mysql5.7
c46bb66ab7bf   redis:latest   "docker-entrypoint.s…"   4 days ago       Exited (0) 24 hours ago                 lucid_heyrovsky
# 把容器内的数据拷贝出来
zq@ZQ:/home$ docker cp 54a05a65a860:/home/bb.java /home
Successfully copied 1.54kB to /home
open /home/bb.java: permission denied
# 把容器内的数据拷贝出来
zq@ZQ:/home$ sudo docker cp 54a05a65a860:/home/bb.java /home
Successfully copied 1.54kB to /home
zq@ZQ:/home$ ls
aa.java  bb.java  zq

# 拷贝是一个手动过程，未来我们使用 -v 卷的技术，可以实现

```

##### 3.4.7 命令图片
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734616127349-f59d3ac5-9a42-44e3-9968-27576e856a5b.png)

##### 3.4.8 操作实践
###### 3.4.8.1 docker 安装nginx
```shell
Docker 安装nginx
# 1.搜索镜像 search
# 2.下载镜像 pull
# 3.运行测试

zq@ZQ:~$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
nginx        latest    66f8bdd3810c   3 weeks ago     192MB
redis        latest    b5e874b32a79   2 months ago    117MB
mysql        5.7       5107333e08a8   12 months ago   501MB
centos       latest    5d0da3dc9764   3 years ago     231MB

# -d 后台运行
# --name  给容器命名
# -p 宿主机端口:容器内端口
zq@ZQ:~$ docker run -d --name nginx01 -p 3344:80 nginx
7c07e018344a28e1481293c84acc14ae6d42457d03762d740610edd84f8146d6
zq@ZQ:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                  NAMES
7c07e018344a   nginx     "/docker-entrypoint.…"   5 seconds ago   Up 4 seconds   0.0.0.0:3344->80/tcp   nginx01
zq@ZQ:~$ curl localhost:3344
<!DOCTYPE html>

# 进入容器
zq@ZQ:~$ docker exec -it nginx01 /bin/bash
root@7c07e018344a:/# whereis nginx
nginx: /usr/sbin/nginx /usr/lib/nginx /etc/nginx /usr/share/nginx
```

思考：我们每次改动nginx配置文件，都需要进入容器内部？十分的麻烦，我要是可以在容器外部提供一个映射路径，达到在容器修改文件名，容器内部就可以自动修改？ -v 数据卷！

###### 3.4.8.2 安装tomcat
```shell
# 官方的使用
$ docker run -it --rm tomcat:9.0

# 我们之前的启动都是后台，停止了容器之后，容器还是可以查到 docker run -it --rm, 一般用来测试，用完就删除

# 下载再启动
docker pull tomcat

# 启动运行
docker run -d -p 3355:8080 --name tomcat01 tomcat

# 测试访问没有问题

# 进入容器
docker exec -it tomcat01 /bin/bash

# 发现问题， 1.很多命令都不支持，只下载最小镜像 2.没有webapps
# 保证最小可运行镜像
```

也是需要把相关的文件映射出来。

###### 3.4.8.3 安装达梦8数据库
去达梦官网下载docker安装包，拷贝到 D:\devTools\dockerData\downloadImages 路径下

[https://eco.dameng.com/document/dm/zh-cn/start/dm-install-docker.html](https://eco.dameng.com/document/dm/zh-cn/start/dm-install-docker.html)

```shell
# 执行安装命令
docker load -i dm8_20240422_x86_rh6_64_rq_std_8.1.3.100_pack2.tar

# 安装成功， 测试启动
docker run -d -p 5236:5236 --restart=always --name=dm8 --privileged=true -e LD_LIBRARY_PATH=/opt/dmdbms/bin -e PAGE_SIZE=16 -e EXTENT_SIZE=32 -e LOG_SIZE=1024 -e UNICODE_FLAG=1  -e INSTANCE_NAME=dm8 -e SYSDBA_PWD=dameng1234 -e=CASE_SENSITIVE=0 -volume=D:\devTools\dockerData\volume\dm8\data:/opt/dmdbms/data dm8_single:dm8_20241022_rev244896_x86_rh6_64


```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734867567923-aa660ede-d942-4b33-9c87-d3f85cfe2888.png)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734867581177-223f28c2-77e0-4c6e-b550-f53f9b0d92e5.png)

启动参数配置说明

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734867736384-bd29be24-4179-4405-a9c9-cbbcf2a97d49.png)

配置启动参数

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734868637574-87656803-5eb7-44f9-bc57-03594bcd350b.png)

连接成功

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734869542630-5fa520bb-d355-4a24-adce-f0c76fef06dc.png)



###### 3.4.8.4 安装fastdfs服务
```shell
docker search fastdfs
docker pull dalron/fastdfs
docker images
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734872411823-2efeb414-78a2-41b6-b992-965011acb436.png)

**构建 Tracker 服务**

```shell
# 通过 docker 命令创建 Tracker服务(不适用于Windows)
docker run -dti --name tracker --network=host -volume=D:\devTools\dockerData\volume\fastdfs\tracker:/var/fdfs dalron/fastdfs tracker
# tracker 服务默认的端口是22122， -v 实现了容器和本地目录的挂载操作
```

**构建Storage 服务**

```shell
# 接下来创建Storage 服务，命令如下
docker run -dti --name storage --network=host -e TRACKER-SERVER=host.docker.internal:22122 -volume=D:\devTools\dockerData\volume\fastdfs\storage:/var/fdfs -e GROUP_NAME=group1 dalron/fastdfs storage
# 执行上述命令时需注意，其中 TRACKER-SERVER 的ip需要修改为你的 Tracker 服务所在的服务IP地址
```

| 服务 | 默认端口 |
| --- | --- |
| tracker | 22122 |
| storage | 23000 |
| Nginx | 8888 |


**windows安装**

```shell
# windows里面不能像Linux一样用 --network=host 这样来设置
所以先搭建自定义网络
docker network create fastdfs_network
```

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1735969729183-e13e6f79-de79-49ad-a534-9ab95c605f1c.png)

```shell
# 创建tracker服务
docker run -it -d --name fastdfs_tracker -h tracker --network=fastdfs_network -p 22122:22122 --volume=/mnt/d/devTools/dockerData/volume/fastdfs/tracker:/var/fdfs delron/fastdfs:latest tracker 

# 创建storage服务
docker run -it -d --name fastdfs_storage -h storage --network=fastdfs_network -p 8888:8888 -p 23000:23000 -e TRACKER_SERVER=host.docker.internal:22122 --volume=/mnt/d/devTools/dockerData/volume/fastdfs/storage_contract:/var/fdfs --volume=/mnt/d/devTools/dockerData/volume/fastdfs/storage:/var/fdfs2 delron/fastdfs:latest storage 

# 当有多个存储空间时 使用下方这个
docker run -it -d --name fastdfs_storage -h storage --network=fastdfs_network -p 8888:8888 -p 23000:23000 -e TRACKER_SERVER=host.docker.internal:22122 --volume=/mnt/d/devTools/dockerData/volume/fastdfs/storage:/var/fdfs --volume=/mnt/d/devTools/dockerData/volume/fastdfs/storage_contract:/var/fdfs2 delron/fastdfs:latest storage 

# 如果有多个存储路径，记得修改配置文件 （storage容器的 /etc/fdfs/storage.conf 文件的配置）
store_path_count=2
store_path0=/var/fdfs
store_path1=/var/fdfs1
# 对应应用也要设置要走哪个目录
# 设置完成之后记得重启应用
```

多目录配置文件

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736585983169-a37ebb56-0ca9-466d-8ed2-0e19652a6c99.png)

设置走 1 目录

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736586149108-eee9aeb1-187c-4a8e-9feb-d45fe91479a2.png)

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736500386991-5ae71387-aee3-4193-b321-e36d3638bf95.png)

如图表示启动成功：

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736501004963-0c88e82d-0370-4a24-9662-d1449d40b127.png)

测试下：

在挂载目录上 D:\devTools\dockerData\volume\fastdfs\storage 创建一个测试文件 test.txt

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736501073022-befc46ef-bc89-401b-b6fa-a91a1d7998d2.png)

之后可以在docker上看到文件成功出现

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736501114151-82f46d86-df5f-4337-a3d7-ac3a17b920a0.png)

我们在容器终端执行:

```shell
# 上传文件
fdfs_upload_file /etc/fdfs/client.conf /var/fdfs/test.txt
```

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736501229189-2b948b4b-7108-4189-8319-1cc6e14418c8.png)

对应位置成功出现，测试成功！

![](https://cdn.nlark.com/yuque/0/2025/png/22229609/1736501278736-ad55cac5-6ee9-4446-8522-578dae1e28e7.png)

部署到应用上时，因为创建的是docker自定义网络，所以外部应用访问不到 172.18.0.3:23000 （docker自定义网络）而导致无法上传和下载文件。可以在外部应用建立对应关系，把 172.18.0.3 转换成本地地址 127.0.0.1 之后就可以成功上传和下载文件。







###### 3.4.8.5 部署 es + kibana
```shell
# es 暴露的端口很多！
# es 十分的耗内存
# es的数据一般需要放置到安全目录！挂载
# --net somenetwork ? 网络配置

# 启动 elasticsearch
docker run -d --name elasticsearch -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:7.6.2

# 启动了 linux 就卡住了
docker stats 查看 cpu 状态

# es 是十分耗内存的， 1.xG  1核2G！

# 太卡的话，赶紧关闭， 然后增加一些内存的限制， 修改配置文件 -e 环境配置修改
docker run -d --name elasticsearch -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -e ES_JAVA_OPTS="-Xms64m -Xmx512m" elasticsearch:7.6.2 

问题：kibana 怎么连接 es？

```

下面这个怎么连啊？

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734619006322-c4da5a72-768e-4477-9753-b89e83391e53.png)

###### 3.4.8.6 可视化
+ portainer（先用这个）
+ Rancher（CI/CD再用）

什么 portainer ? 

Docker图形化界面管理工具！提供一个后台面板供我们操作

```shell
docker run -d -p 8088:9000 --restart=always -v /var/run/docker.sock:/var/run/docker.sock --privileged=true portainer/portainer
```

访问测试： http://ip:8088

# 四、Docker镜像
### 4.1 镜像是什么
镜像是一种轻量级、可执行的独立软件包，用来打包软件运行环境

### 4.2 镜像加载原理
### 4.3 分层理解
Docker镜像都是只读的，当容器启动时，一个新的可写层被加载到镜像的顶部！

这一层就是我们通常说的容器层，容器之下的都叫镜像层！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734621297508-d43fc300-7295-4aad-9833-3fea648a314d.png)

### 4.4 commit镜像
```shell
docker commit 提交容器成为一个新的副本

# 命令和 git 原理类似
docker commit -m="提交的描述信息" -a="作者" 容器id 目标镜像名:[TAG]

实战测试
# 1.启动一个默认的tomcat
docker run -it -p 8080:8080 --name tomcat02 tomcat /bin/bash
# 2.发现这个默认的tomcat是没有webapps应用，镜像的原因，官方的镜像默认 webapps 为空
# 3.把webapps里面添加内容后
# 4.提交容器， 提交为一个镜像！我们以后就是用我们修改过的镜像即可，这就是我们自己的一个修改的镜像
docker commit -a="zhiq" -m="add webapps app" 容器id tomcat02:1.0

```

如果你想要保存当前容器的状态，就可以通过commit来提交，获得一个镜像。

就好比一个快照。



# 五、容器数据卷
### 5.1 docker的理念回顾
将应用和环境打包成一个镜像！

数据？如果数据都在容器中，那么我们容器删除，数据就会丢失！<font style="color:#DF2A3F;">需求：数据库可以持久化</font>

MYSQL，容器删了，删库跑路！<font style="color:#DF2A3F;">需求：MYSQL数据可以存储在本地！</font>

容器之间可以有一个数据共享的技术！Docker容器中产生的数据，同步到本地！

这就是卷技术！目录的挂在，将我们容器内的目录，挂载到Linux上面！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734768432891-7dc2cca5-a6c1-464e-a6f8-d59dbb5db31c.png)

**总结一句话：容器的持久化和同步操作！容器见也是可以数据共享的！**

### 5.2 使用数据卷
**方式1：使用命令挂载 -v**

```shell
docker run -it -v 主机目录:容器内目录

# 测试
zq@ZQ:/mnt/d/devTools/dockerData$ docker run -it -v /mnt/d/devTools/dockerData/volume/ceshi:/home centos /bin/bash

# 启动起来之后我们可以通过 docker inspect 容器id
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734768992957-fe0b720c-afb9-474c-82ae-af0a95f2515c.png)

测试文件的同步

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734769124566-c8c1ae0b-15b4-4977-8e3c-0120ca7284eb.png)

再来测试：1.停止容器。2.宿主机上修改文件。3.启动容器。4.容器内的数据依旧是同步的。

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734769382321-d5dbb40c-436f-4b9c-99e9-4cd02889d6ca.png)

好处：我们以后修改只需要在本地修改即可，容器内会自动同步！

### 5.3 实战：安装MYSQL
思考： MYSQL的数据持久化的问题!

```shell
# 获取镜像
docker pull mysql:5.7

# 运行容器，需要做数据挂载 
# 安装启动 mysql，需要配置默认的密码
$ docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag

# 启动我们的
-d 后台运行
-p 端口映射
-v 数据卷挂载
-e 环境配置
--name 容器名称
zq@ZQ:/mnt/d/devTools/dockerData$ docker run -d -p 3306:3306 -v /mnt/d/devTools/dockerData/volume/mysql/conf:/etc/mysql/conf.d -v /mnt/d/devTools/dockerData/volume/mysql/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 --name mysql01 mysql:5.7

# 如果是windows系统启动的话，还是要用工具启动，然后复制他的启动命令如下：(😄)
docker run --hostname=bac741eb7fa6 --mac-address=02:42:ac:11:00:02 --env=MYSQL_ROOT_PASSWORD=123456 --env=PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin --env=GOSU_VERSION=1.16 --env=MYSQL_MAJOR=5.7 --env=MYSQL_VERSION=5.7.44-1.el7 --env=MYSQL_SHELL_VERSION=8.0.35-1.el7 --volume=D:\devTools\dockerData\volume\mysql\conf:/etc/mysql/conf.d --volume=D:\devTools\dockerData\volume\mysql\data:/var/lib/mysql --volume=/var/lib/mysql --network=bridge -p 3306:3306 -p 33059:33060 --restart=no --runtime=runc -d mysql:5.7

# 启动成功之后，可以测试一下，测试成功！

# 在本地创建一个数据库，查看一下我们映射的路径是否ok！
```

假设我们将容器删除，发现我们挂载到本地的数据卷依旧没有丢失，这就实现了容器数据持久化功能！

### 5.4 具名和匿名挂载
```shell
# 匿名挂载
-v 容器内路径
docker run -d -p --name nginx01 -v /etc/nginx nginx

# 查看所有的 volume 的情况
docker volume ls

#这里发现，这种就是匿名挂载，我们在 -v 只写了容器内的路径，没有写容器外的路径

#具名挂载
docker run -d -p --name nginx02 -v juming-nginx:/etc/nginx nginx
docker volume ls

# 通过 -v 卷名:容器内瑞金
# 查看一下这个卷

```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734776432370-e2b20d4e-822f-4f81-a2d8-9d79385dcae4.png)

所有的docker容器内的卷，没有指定目录的情况下都是在 `/var/lib/docker/volumes/xxx/_data`

我们通过具名挂载可以和hi方便的找到我们的一个卷，大多数情况在使用的 `具名挂载`

```shell
# 如何确定是具名挂载还是匿名挂载，还是指定路径挂载
-v 容器内路径 	  # 匿名挂载
-v 卷名:容器内路径 	# 具名挂载
-v /宿主机路径：容器内路径  # 路径挂载
```

拓展：

```shell
# 通过 -v 容器内路径，ro  rw 改变读写权限
ro   readonly  # 只读
rw 	 readwrite 	# 只读可写

# 一旦设定了这个容器全新啊，容器对我们挂载出来的内容就有限定了
docker run -d -p --name nginx02 -v juming-nginx:/ect/nginx:ro nginx
docker run -d -p --name nginx02 -v juming-nginx:/ect/nginx:rw nginx

# ro 只要看到ro就说明这个路径只能通过宿主机来操作，容器内部是无法操作的。
```

### 5.5 初识DockerFile
Dockerfile 就是用来构建 docker 镜像的构建文件！ 命令脚本！

通过这个脚本可以生成镜像，镜像是一层一层的，脚本一个个的命令，每个命令都是一层！

```shell
# 创建一个dockerfile文件，名字可以随机 建议 Dockerfile

#文件中的内容 指令（大写） 参数
FROM centos
VOLUME ["volume01","volume02"]   # 匿名挂载

CMD echo "----end----"
CMD /bin/bash

# 这里的每个命令，就是镜像的一层！
docker build -f docker路径文件 -t zhiq/centos:1.0 .

```

### 5.6 数据卷容器
多个mysql 同步数据！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734807047806-7c944afd-eec1-4fcd-b470-c3992b484aa8.png)

```shell
# 通过 --volumes-from 可以实现多个容器的数据卷同步
docker run -it --name docker01 zhiq/centos:1.0
docker run -it --name docker02 --volumes-from docker01 zhiq/centos:1.0
docker run -it --name docker03 --volumes-from docker03 zhiq/centos:1.0

# 三个容器的数据卷是共享的。
# 测试，如果删除了 docker01容器， docker02,docker03容器的挂载的数据卷还在，没有被删掉。

```

多个 MySQL 数据共享。

```shell

$ docker run -d --name mysql01 -e MYSQL_ROOT_PASSWORD=123456 mysql:tag

docker run -d --name mysql02 -e MYSQL_ROOT_PASSWORD=123456 --volumes-from mysql01 mysql:tag

# 这个时候，可以实现两个容器数据同步！
```

结论：

容器之间配置信息的传递，数据卷容器的生命周期一直持续到没有容器使用为止。

但是一旦你持久化到了本地，这个时候，本地的数据是不会删除的。

# 六、DockerFile
### 6.1 DockerFile介绍
dockerFIle 是用来构建docker镜像的文件！命令参数脚本！

构建步骤：

1、编写一个 dockerfile 文件

2、docker build 构建成为一个镜像

3、docker run 运行镜像

4、docker push 发布镜像（DockerHub、阿里云镜像库）

看一下官方是怎么做的

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734808717975-9a3a69e5-6145-4089-98cf-587608aa8cf5.png)

很多官方镜像都是基础包，很多功能没有，我们通常会自己搭建自己的镜像！

官方既然可以制作镜像，那我们也可以！

### 6.2 DockerFile构建过程
**基础知识:**

1、每个保留关键字（指令）都是必须是大写字母

2、执行从上到下顺序执行

3、#表示注释

4、每一个指令都会创建提交一个新的镜像层，并提交！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734808997422-9edeb9df-81da-43da-98b4-1cc821f9daf4.png)

dockerfile是面向开发的，我们以后要发布项目，做镜像，就需要编写dockerfile文件，这个文件十分简单！

Docker镜像 逐渐成为了企业交付的标准，必须要掌握！

步骤：开发、部署、上线运维。。缺一不可！

DockerFile：构建文件，定义了一切的步骤，源代码

DockerImages：通过DockerFile构建生成的镜像，最终要发布和运行的产品

Docker容器：容器就似乎镜像运行起来提供服务的。

### 6.3 DockerFile指令
以前的话我们就是使用别人的，现在我们知道了这些指令后，就可以自己写

```shell
FROM					# 基础镜像，一切从这里开似乎  centos
MAINTAINER 		# 镜像是谁写的，姓名+邮箱
RUN 					# 镜像构建的时候需要运行命令
ADD						# 步骤，tomcat镜像， 这个tomcat压缩包！添加内容
WORKDIR				# 镜像的工作目录 
VOLUME 				# 挂载的目录
EXPOSE 				# 对外提供的端口配置
CMD 					# 指定这个容器启动的时候要运行的命令，只有最后一个会生效，可被替代 
ENTRYPOINT 		# 指定这个容器启动的时候要运行的命令，可以追加命令
ONBUILD 			# 当构建一个被继承 DockerFile 这个时候就会运行 ONBUILD 的指令，触发指令
COPY 					# 类似ADD，将我们的文件拷贝到镜像中
ENV 					# 构建的时候设置环境变量！

```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1734809303653-8a8b5b36-8a83-4d0a-935b-070b22382d9e.png)

### 6.4 实战测试
DockerHub中 99% 的镜像都是从这个基础镜像过来的 FROM scratch, 然后配置需要的软件和配置来进行的构建

```shell
# 1.编写dockerfile文件
FROM centos
MAINTAINER zhiq<17090315867@163.com>

ENV MYPATH /usr/local
WORKDIR $MYPATH

RUN yum -y install vim
RUN yum -y install net-tools

EXPOST 80

CMD echo $MYPATH
CMD echo "----end----"

# 2.通过这个文件构建镜像
# 命令 docker build -f dockerfile文件路径 -t 镜像名:[tag]
Successfully build ejiafo83yr

# 3.测试运行
```

### 6.5 制作镜像
### 6.6 发布自己的镜像
1. 地址 [https://hub.docker.com/](https://hub.docker.com/)
2. 确定账号可以登录
3. 在我们服务器上提交自己的镜像

```shell
docker login --help

zq@ZQ:~$ docker login --help

Usage:  docker login [OPTIONS] [SERVER]

Authenticate to a registry.
Defaults to Docker Hub if no server is specified.

Options:
  -p, --password string   Password
      --password-stdin    Take the password from stdin
  -u, --username string   Username
# 登录命令
docker login -u xxx
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735054991419-f11d2a90-d8d3-4d7f-bfb4-ed88793a1ccc.png)

4. 登录完毕后就可以提交镜像了，就是一部 docker push

```shell
# 自己发布的镜像尽量添加上版本号
docker push 自己的镜像名称:版本号
# 给镜像添加版本号
docker tag xx镜像idxxx 敬香茗:版本号

```

> 阿里云镜像
>

1. 登录阿里云
2. 找到容器镜像服务
3. 创建命名空间
4. 创建容器镜像仓库
5. 浏览页面信息（页面上有操作文档：登录、拉去pull、推送push）

### 6.7 小结
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735055693554-0f47a884-4ccd-4cd7-9e0a-4d0361d65fce.png)

# 七、Docker网络原理
### 7.1 理解Docker0
![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735056122225-0e9e0568-c1e4-4b79-9782-5aac95a58014.png)

```shell
# 问题： docker 是如何处理容器网络访问的？

zq@ZQ:~$ docker run -d -P --name tomcat01 tomcat:7.0
Unable to find image 'tomcat:7.0' locally

7.0: Pulling from library/tomcat
0bc3020d05f1: Pull complete
a110e5871660: Pull complete
83d3c0fa203a: Pull complete
a8fd09c11b02: Pull complete
96ebf1506065: Pull complete
26b72ffca293: Pull complete
0bffa2ea17aa: Pull complete
d880cebcc7a6: Pull complete
d19ab8039b36: Pull complete
5057492dc495: Pull complete
Digest: sha256:f7d37d248d0eacec1e5995736234c9c22155626fcb27ea3ead13b9db24e698f7
Status: Downloaded newer image for tomcat:7.0
fec0dfda37c545607a780605c73a74878b38c07e4699f29fa01a46d1f2193a9a
zq@ZQ:~$
zq@ZQ:~$ docker ps
CONTAINER ID   IMAGE        COMMAND             CREATED         STATUS         PORTS                     NAMES
fec0dfda37c5   tomcat:7.0   "catalina.sh run"   3 seconds ago   Up 3 seconds   0.0.0.0:32771->8080/tcp   tomcat01
zq@ZQ:~$ docker exec -it tomcat01 ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
25: eth0@if26: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default
    link/ether 02:42:ac:11:00:02 brd ff:ff:ff:ff:ff:ff link-netnsid 0
    inet 172.17.0.2/16 brd 172.17.255.255 scope global eth0
       valid_lft forever preferred_lft forever
zq@ZQ:~$

# 思考： linux能不能 ping 同容器内部
linux可以 ping 通的 

# linux 可以 ping 通 docker 容器内部

```

> 原理
>

1. 我们每启动一个docker容器，docker就会给docker容器分配一个ip，我们只要安装了docker，就会有一个网卡 docker0 桥接模式，使用的技术是 evth-pair 技术！
2. 再启动一个容器测试，发现又多了一对网卡~！

```shell
# 我们发现这个容器带来网卡，都是一对一对的
# evth-pair 就是一堆的虚拟设备接口，他们都是成对出现的，一段连着协议，一段彼此相连
# 正因为有这个特性，evth-pair 充当一个桥梁，连接各种虚拟网络设备的
# OpenStac, Docker 容器之间的连接， OVS的连接，都是使用的 evth-pair 技术
```

3. 我们测试 tomcat01 和 tomcat02 是否可以 ping 通，

```shell
# 以下发现 容器和容器之间是可以相互 ping 通的。
zq@ZQ:~$ docker exec -it tomcat02 ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
7: eth0@if8: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default
    link/ether 02:42:ac:11:00:03 brd ff:ff:ff:ff:ff:ff link-netnsid 0
    inet 172.17.0.3/16 brd 172.17.255.255 scope global eth0
       valid_lft forever preferred_lft forever
zq@ZQ:~$ docker exec -it tomcat02 ping 172.17.0.2
PING 172.17.0.2 (172.17.0.2) 56(84) bytes of data.
64 bytes from 172.17.0.2: icmp_seq=1 ttl=64 time=0.162 ms
64 bytes from 172.17.0.2: icmp_seq=2 ttl=64 time=0.084 ms
64 bytes from 172.17.0.2: icmp_seq=3 ttl=64 time=0.074 ms
^C
--- 172.17.0.2 ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 84ms
rtt min/avg/max/mdev = 0.074/0.106/0.162/0.041 ms
```

绘制一个网络模型图。

结论：tomcat01 和 tomcat02 是共用的一个路由器，docker0

所有的容器不指定网络的情况下，都是docker0 路由的，docker会给我们的容器分配一个默认的可用IP

> 小结
>

Docker 使用的是Linux的桥接，宿主机中是一个Docker容器的网桥 docker0

Docker中的所有的网络接口都是虚拟的，虚拟的妆发效率高！（内网传递文件）

只要容器删除，对应网桥一对就没了！

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735060132539-7616abd2-c44e-4ffa-9696-067547e73852.png)

### 7.2 --link
```shell
zq@ZQ:~$ docker exec -it tomcat01 ping tomcat02
ping: tomcat02: No address associated with hostname

# 如何解决
# 通过 --link 既可以解决了网络连通问题
zq@ZQ:~$ docker run -d -P --name tomcat03 --link tomcat02 tomcat:7.0
cfea9fbd0d28b38533b215ce5562353cd22745d07ba318dd993758a06e4747f0
zq@ZQ:~$ docker exec -it tomcat03 ping tomcat02
PING tomcat02 (172.17.0.3) 56(84) bytes of data.
64 bytes from tomcat02 (172.17.0.3): icmp_seq=1 ttl=64 time=0.205 ms
64 bytes from tomcat02 (172.17.0.3): icmp_seq=2 ttl=64 time=0.065 ms
^C
--- tomcat02 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 80ms
rtt min/avg/max/mdev = 0.065/0.135/0.205/0.070 ms
zq@ZQ:~$

# 反向 ping 不通
zq@ZQ:~$ docker exec -it tomcat02 ping tomcat03
ping: tomcat03: No address associated with hostname

```

探究：

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735060154081-304d86de-f5f1-4a62-8049-5a5aeaa18a03.png)

其实这个tomcat03 就是在本地配置了 tomcat02 的配置

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735060406846-8909d758-0c22-42b2-92f7-54718f96a53d.png)

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735060443808-bdcc6617-a5ea-4336-84dc-b2227aa72eaf.png)

我们现在玩 Docker 已经不建议使用 --link 了！

自定义网络！不适用 docker0

docker0问题：他不支持容器名连接访问！

### 7.3 自定义网路
> 查看所有的docke网络
>

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735297361977-e0c6f98f-c64b-43ba-9c4d-15662d659576.png)

**网络模式**

bridge:   桥接 docker （默认，自己创建也使用 bridge 模式）

none：   不配置网络

host：	和宿主机共享网络

container:	容器网络联通！（用的少！局限很大！）

测试

```shell
# 我们直接启动的命令 --net bridge， 而这个就是我们的docker0
docker run -d -P --name tomcat01 tomcat
docker run -d -P --name tomcat01 --net bridge tomcat

# docker0 特点， 默认，域名不能访问，  --link可以大同连接

# 我们可以自定义一个网络
# --driver bridge
# --subnet 192.168.0.1/16
# --gateway 192.168.0.1
docker network create --driver bridge --subnet 192.168.0.0/16 --gateway 192.168.0.1 mynet
```

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735297787735-39eed73c-50f2-4c95-b881-e0b549710a7a.png)

自己的网络就创建好了

![](https://cdn.nlark.com/yuque/0/2024/png/22229609/1735297895763-b1d0d427-7c7e-43df-b59c-5a07762abf7a.png)

```shell

zq@ZQ:~$ docker run -d -P --name tomcat-net-01 --net mynet tomcat:7.0
b7efccecda69dd2e73155de6a168b69668f8473042de263eaed3a4f93cbe363f
zq@ZQ:~$ docker ps
CONTAINER ID   IMAGE        COMMAND             CREATED         STATUS         PORTS                     NAMES
b7efccecda69   tomcat:7.0   "catalina.sh run"   3 seconds ago   Up 3 seconds   0.0.0.0:32768->8080/tcp   tomcat-net-01
zq@ZQ:~$ docker run -d -P --name tomcat-net-02 --net mynet tomcat:7.0
d97c059633ffa5dfc4109efa4af189f32cdcb7beaf37efbced403339971761e8
zq@ZQ:~$ docker network inspect mynet
[
    {
        "Name": "mynet",
        "Id": "9191aa296b4ba4e42f2167747b786e325dc39a69a52f9d0e77cbfb44bfb43ab4",
        "Created": "2024-12-27T11:09:32.934462061Z",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": {},
            "Config": [
                {
                    "Subnet": "192.168.0.0/16",
                    "Gateway": "192.168.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {
            "b7efccecda69dd2e73155de6a168b69668f8473042de263eaed3a4f93cbe363f": {
                "Name": "tomcat-net-01",
                "EndpointID": "30a5b6993b134e791de9fa707bbea3d9a4d1130e20d6a732e960a64361638e70",
                "MacAddress": "02:42:c0:a8:00:02",
                "IPv4Address": "192.168.0.2/16",
                "IPv6Address": ""
            },
            "d97c059633ffa5dfc4109efa4af189f32cdcb7beaf37efbced403339971761e8": {
                "Name": "tomcat-net-02",
                "EndpointID": "8390bb812f173f126be38d85273652f61a5031dd9d608eda9aa93176f5db2864",
                "MacAddress": "02:42:c0:a8:00:03",
                "IPv4Address": "192.168.0.3/16",
                "IPv6Address": ""
            }
        },
        "Options": {},
        "Labels": {}
    }
]

# 再次测试ping连接
zq@ZQ:~$ docker exec -it tomcat-net-01 ping 192.168.0.3
PING 192.168.0.3 (192.168.0.3) 56(84) bytes of data.
64 bytes from 192.168.0.3: icmp_seq=1 ttl=64 time=0.088 ms
64 bytes from 192.168.0.3: icmp_seq=2 ttl=64 time=0.081 ms
^C
--- 192.168.0.3 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 52ms
rtt min/avg/max/mdev = 0.081/0.084/0.088/0.009 ms

# 现在不适用 --link 也可以ping名字
zq@ZQ:~$ docker exec -it tomcat-net-01 ping tomcat-net-02
PING tomcat-net-02 (192.168.0.3) 56(84) bytes of data.
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=1 ttl=64 time=0.053 ms
64 bytes from tomcat-net-02.mynet (192.168.0.3): icmp_seq=2 ttl=64 time=0.085 ms
^C
--- tomcat-net-02 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 56ms
rtt min/avg/max/mdev = 0.053/0.069/0.085/0.016 ms
```

我们自定义的网络docker 都已经帮我们维护好了对应的关系，推荐我们平时这样使用网络！

好处：

redis - 不同的集群使用不同的网络，保证集群是安全和健康的。

### 7.4 网络连通
```shell
# 测试打通 tomcat01 到 tomcat-net-01

docker network connect mynet tomcat01

# 连通之后就是将 tomcat01  放到了 mynet  网络下

# 一个容器两个ip地址
```

结论： 假设要跨网络操作别人，就需要使用 docker network connect 连通 ！

### 7.5 部署redis集群
```shell
# 3主3从
docer network create network redis --subnet 172.38.0.0/16

# 通过脚本创建六个redis配置
for port in $(seq 1 6); \
do \
mkdir -p /mydata/redis/node-${port}/conf/redis.conf
cat << EOF >>/mydata/redis/node-${port}/conf/redis.conf
port 6379
bind 0.0.0.0
cluster-enable yes
cluster-config-file nodes.conf
cluster-announce-ip 172.38.0.1${port}
cluster-announce-port 6379
cluster-announcce-bus-port 16379
appendonly yes
EOF
done

# 以下命令 修改后要创建6个
docker run -p 6371:6379 -p 16371:16379 --name redis-1 \
-v /mydata/redis/node-1/data:/data \
-v /mydata/redis/node-1/redis.conf:/etc/erdis/redis.conf \
-d --net redis --ip 172.38.0.11 redis:5.0.9-alpine3.11 redis-server /etc/redis/redis.conf

# 创建集群
redis-cli --cluster create 172.38.0.11:6379 172.38.0.12:6379 ... 172.38.0.16:6379 --cluster-replicas 1
```

### 7.6 SpringBoot微服务打包Docker镜像
1、构建springboot项目

2、打包应用

3、编写dockerfile

4、构建镜像

5、发布运行！



以后我们使用了Docker之后，给别人交付的就是一个镜像即可！

到了这里我们已经完全够用了Docker！



预告：如果有很多镜像，100个？



# 八、Docker Compose
# 九、Docker Swarm
# 十、CI\CD Jenkins


即使再小的帆，也能远航。


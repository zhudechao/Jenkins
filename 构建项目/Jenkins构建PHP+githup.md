# Jenkins构建PHP+githup

##### 1:安装插件

```
git
githup
Publish Over SSH
```

##### 2:配置Publish over SSH

```
key 是 jenkins服务器 ssh-keygen 生成的私钥
.ssh]# cat id_rsa
把公钥传到php服务器上
.ssh]# scp id_rsa.pub root@xx.xx.xx.xx:/root/.ssh/id_rsa01

在php服务器上进行操作
.ssh]# cat id_rsa01 >> authorized_keys
```

![](/images/001.jpg)

##### 3:创建任务

![](.\images\002.jpg)

##### 4:配置

![](.\images\003.jpg)

![](.\images\004.jpg)

![](.\images\005.jpg)
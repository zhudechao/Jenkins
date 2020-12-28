# Jenkins安装

前置环境

```
安装以下环境
java jdk
git

下载jenkins rpm安装包
下载地址:http://mirrors.jenkins-ci.org/redhat/
wget http://mirrors.jenkins-ci.org/redhat/jenkins-2.269-1.1.noarch.rpm
```

安装Jenkins

```bash
software]# wget http://mirrors.jenkins-ci.org/redhat/jenkins-2.269-1.1.noarch.rpm
software]# rpm -ivh jenkins-2.269-1.1.noarch.rpm
```

配置Jenkins

```bash
software]# cd /etc/sysconfig
sysconfig]# vi jenkins

JENKINS_USER="root"
JENKINS_PORT="8888"
```

启动Jenkins

```bash
sysconfig]# systemctl start jenkins
```

运行出错解决

```
错误描述
Job for jenkins.service failed because the control process exited with error code. See "systemctl status jenkins.service" and "journalctl -xe" for details.

sysconfig]# vi /etc/init.d/jenkins

#/usr/bin/java
/usr/java/jdk1.8.0_212/bin/java
```

访问Jenkins界面

```
http://8.210.66.245:8888/
```

初始密码

```
sysconfig]# cat /var/lib/jenkins/secrets/initialAdminPassword
9852b2e1df92462793c80597dd6dab59
```

修改url

```
jenkins.xzdream.cn:8888
```


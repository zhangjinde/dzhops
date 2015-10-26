# dzhops   
+ 使用Django框架开发的Salt Stack Web UI   

##环境：
+ RHEL 6.5 x86_64
+ salt-master 2015.5.3    
+ salt-minion 2015.5.3      
+ salt-api 2015.5.3（此版本已合并到主分支）     
+ Django 1.6.8     
+ python 2.6.6     
+ MySQL 5.5  
+ 网卡流量图使用rrdtool(v1.3.8)工具

## 功能介绍
1.**首页**，显示SaltMaster所在服务器及相关组件状态信息
![首页](https://github.com/Hasal/picture/blob/master/dzhops_pic/index.png)
1.**认证信息**
![认证信息](https://github.com/Hasal/picture/blob/master/dzhops_pic/au.png)
2.**模块部署-返回结果**，蓝色表示执行成功，红色表示有失败存在，可以点击标签查看详细情况
![模块部署-返回结果](https://github.com/Hasal/picture/blob/master/dzhops_pic/deploy.png)
3.**模块部署-返回结果详情查看（1）**
![模块部署-返回结果详情查看（1）](https://github.com/Hasal/picture/blob/master/dzhops_pic/deploy-dec-1.png)
4.**模块部署-返回结果详情查看（2）**
![模块部署-返回结果详情查看（2）](https://github.com/Hasal/picture/blob/master/dzhops_pic/deploy-dec-2.png)
5.**配置更新**-执行结果返回显示格式与模块部署相似
![配置更新](https://github.com/Hasal/picture/blob/master/dzhops_pic/config_update.png)
6.**远程命令执行**
![远程命令执行](https://github.com/Hasal/picture/blob/master/dzhops_pic/exec.png)
7.**主机列表信息**
![主机列表信息](https://github.com/Hasal/picture/blob/master/dzhops_pic/server_list.png)

##计划任务设定
+ */5 * * * * /tmp/get_eth0_traffic.sh
+ */10 * * * * /var/www/dzhops/scripts/data_acquisition.py
+ */10 * * * * /var/www/dzhops/scripts/prc.py
+ */10 * * * * /var/www/dzhops/scripts/slapi.py

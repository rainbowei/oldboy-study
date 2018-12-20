
作者| 孙科伟
---|---
Email|sunkeweimail@163.com
QQ | 1419266210

---

学习login的登陆和注册，注销。以及django的表单操作。
[参考文档](https://www.cnblogs.com/maple-shaw/p/7464131.html)

---

### 1 django.contrib.auth类
微信公众号官网：https://qy.weixin.qq.com/
我们主要获取四个参数：部门id，应用ID和CorpID和CorpSecret
#### 1.1  authenticate()方法
注册微信企业号，安装手机微信略过
#### 1.2 login()方法
在通信录管理里面设置部门，如下图，我们这里设置的运维部，这个部门id要记住，在ZABBIX里面要配置这个名称，然后把你需要发送告警的人员添加到这个部门里面
### 1.3 logout()方法
点击左侧“应用中心”，新建消息型应用，应用名称为“服务器报警”，“应用可见范围”，添加刚刚新建的子部门（运维部），点击“服务器报警”，记录应用ID

### 2 代码演示
代码托管到github：https://github.com/bluetom520/zabbix-weixin-picture
下载
```
git clone https://github.com/bluetom520/zabbix-weixin-picture.git
```
依赖包
```



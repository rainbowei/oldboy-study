
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

### 3 ZABBIX配置
#### 3.1 报警媒介类型
到管理-》报警媒介类型配置我们的微信
![](leanote://file/getImage?fileId=587386aa4f1ffe4e59000001)
#### 3.2 配置用户
到管理-》用户-》报警媒介-》添加，注意填写收件人为我们之前设置的运维部id 2
![](leanote://file/getImage?fileId=587386cf4f1ffe4e59000002)
#### 3.3 动作设置
到配置-》动作-》创建动作（触发器）
 - 动作
![](leanote://file/getImage?fileId=587089ffd31d9c3103000006)

 - 条件
![](leanote://file/getImage?fileId=58708a1dd31d9c3103000007)
 - 操作
![](leanote://file/getImage?fileId=587386fb4f1ffe4e59000003)

### 4 效果展现
故障图
![](leanote://file/getImage?fileId=5874b25d2eb3ec5799000005)
恢复图
![](leanote://file/getImage?fileId=5874b2292eb3ec5799000004)

### 5 docker环境修改
> * 参照无图版


### 如果你觉得微信报警对你有帮助, 可以对作者进行小额捐款(微信)

![weixin](weixin.jpg)



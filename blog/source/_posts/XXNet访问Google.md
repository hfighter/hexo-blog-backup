---
title: XX-Net 是在国内能够访问Google的一种方式
tags: [工具, 技巧, 翻墙]
categories: 工具
---


##### 一、XX-Net 是在国内能够访问Google的一种方式。
##### 二、配置XX-Net大致需要以下几个步骤
 - 1、Google账号(Google邮箱账号)，此步骤比较简单，在此不做说明
 - 2、下载XX-Net👉[`猛戳`](https://github.com/XX-net/XX-Net)，然后安装，安装步骤👉[`猛戳`](https://github.com/XX-net/XX-Net/wiki/%E4%BD%BF%E7%94%A8Chrome%E6%B5%8F%E8%A7%88%E5%99%A8)
 - 3、在Google上创建AppId，步骤👉[`猛戳`](https://github.com/XX-net/XX-Net/wiki/how-to-create-my-appids)
 - 4、部署服务端，步骤👉[`猛戳`](https://github.com/XX-net/XX-Net/wiki/how-to-create-my-appids) 的下半文
 - 5、其它参考👉[`猛戳`](https://gochrome.info/xxnet-tutorial/)

<!--more-->

#### 三、针对以上步骤做以下说明：
1、建议先进行第2步，再进行第3步；由于创建AppId需要访问Google，先安装上XX-Net后，XX-Net自带公用账号，可以访问Google尽管速度慢点😊；
2、对于创建AppId，由于访问比较慢可能费时一些；创建Id地址👉[`猛戳`](https://console.developers.google.com/) ；设置AppID的App引擎👉[`猛戳`](https://console.cloud.google.com/home/)选择刚创建的Id
![设置AppID引擎](http://upload-images.jianshu.io/upload_images/2742404-df6b444c36a63ef3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
3、设置弱网应用许可👉[`猛戳`](https://gochrome.info/wp-content/themes/Begin/inc/go.php?url=https://www.google.com/settings/security/lesssecureapps)
4、设置应用专用密码👉[`猛戳`](https://gochrome.info/wp-content/themes/Begin/inc/go.php?url=https://security.google.com/settings/security/apppasswords)
5、部署服务端，Windows部署相对简单参考文档可以部署成功，Mac参考文档部署不成功，遇到问题可以参考👉[`猛戳`](https://github.com/XX-net/XX-Net/issues) and👉[`猛戳`](https://github.com/XX-net/XX-Net/wiki/%E6%95%85%E9%9A%9C%E9%80%9F%E6%9F%A5%E6%89%8B%E5%86%8C)；Mac下部署我使用的是命令部署的，具体命令如下:
![命令部署](http://upload-images.jianshu.io/upload_images/2742404-f788bc33304046d8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 四、共享电脑的vpn给手机
共享电脑VPN给手机，具体步骤如下，参考👉[`猛戳`](https://github.com/XX-net/XX-Net/issues/2976)：
- 1、将xx-net\code\default\gae_proxy\local\proxy.ini 内容复制\data\gae_proxy\config.ini中并修改config.ini中

```
[pac]
enable = 1
ip = 0.0.0.0
port = 8086
file = proxy.pac
[listen]
ip = 0.0.0.0
port = 8087
visible = 1
debuginfo = 0
```
- 2、手机安装证书，将XX-Net中的CA.crt，发送到邮箱，然后在手机查看邮件安装
- 3、打开XX-Net系统配置 允许远程连接Web控制端，重启XX-Net
- 4、手机端设置代理，HTTP代理选择`自动 `，URL填写：`http://电脑ip:8086/proxy.pac`

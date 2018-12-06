# go2cloud_v1.0.0

## 简介
go2cloud_v1.0.0是为了用户快速的迁移其他共有云厂商实例或虚拟机，IDC物理机到腾讯云的工具。

## 安装
#### 下载
```
yum install -y git || apt-get update && install git -y
git clone https://github.com/redhatxl/go2cloud_v1.0.0.git
cd go2cloud_v1.0.0
```
#### 配置

修改文件`go2cloud_v1.0.0/go2tencent_src/config/user_config.json`
```
{
    "app_id": "1253329830",
    "secret_id": "AKIDZyGQXbErpxxxxxxxxxxxxxxxxxxxxxx",
    "secret_key": "kFUTDk38yZw4xxxxxxxxxxxxxxxxx",
    "region_id": "ap-beijing",
    "image_name": "go2tencent-img",
    "bandwidth_limit": 0,
    "bucket_name": "go2tencent"
}

```
修改内部的app_id为腾讯目的端云账号的appid
添加腾讯云目的端的secretid/secretkey
修改迁移目的端的地域

#### 运行
注意：如若考虑shell终端终端，请放在系统后台执行`chmod +x go2tencent.sh && nohup ./go2tencent.sh &`
在linux系统下运行`go2tencent.sh`

#### 登陆目的端腾讯云账号查看

## 适用

* 适用系统x86：CentOS 6.x/7.x,Ubuntu x,RedHat 6.x/7.x,Debian x
* 腾讯云ak需要具备腾讯云资源开通权限（ECS/VPC/OSS)

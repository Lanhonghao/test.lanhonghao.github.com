# 1.确定版本

首先确定自己的版本是stretch还是jessis

例如：你下载的2017-11-29-raspbian-stretch.zip， 那么就是stretch

执行命令：

```
lsb_release -a     #查看自己的版本类型
```
# 2.stretch版本

## 执行命令(stretch)

```
sudo nano /etc/apt/sources.list 
```
（1）将文件里的默认的官方软件源用# 注释掉 
（2）添加下面的软件源（中国科技大学的软件源 ） （手动添加注意空格）

```
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ stretch main contrib non-free rpi
```
## 执行命令(stretch)

```
sudo nano /etc/apt/sources.list.d/raspi.list 
```
（1）将文件里的默认的官方软件源用# 注释掉 
（2）添加下面的软件源（中国科技大学的软件源 )（手动添加注意空格）

```
deb http://mirrors.ustc.edu.cn/archive.raspberrypi.org/ stretch main ui
```

## 更新

```
sudo apt-get update 
sudo apt-get upgrade
```

# 3.jessis版本

## 执行命令(jessis)

```
sudo   nano  /etc/apt/sources.list 
```
（1）将文件里的默认的官方软件源用# 注释掉 
（2）添加下面的软件源（中国科技大学的软件源 ） （手动添加注意空格）

```
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ jessis main contrib non-free rpi
```

## 执行命令(jessis)

```
sudo  nano  /etc/apt/sources.list.d/raspi.list 
```
（1）将文件里的默认的官方软件源用# 注释掉 
（2）添加下面的软件源（中国科技大学的软件源 )（手动添加注意空格）

```
deb http://mirrors.ustc.edu.cn/archive.raspberrypi.org/ jessis main ui
```

## 更新

```
sudo apt-get update
sudo apt-get upgrade 
```



# 4.开源软件镜像站

清华大学开源软件镜像站：

```
deb http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ jessie main non-free contrib
deb-src http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ jessie main non-free contrib
```

中国科学技术大学Linux用户协会：

```
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ jessie main non-free contrib
deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ jessie main non-free contrib
```

浙江大学开源镜像站：

```
deb http://mirrors.zju.edu.cn/raspbian/raspbian/ jessie main contrib non-free rpi
deb-src http://mirrors.zju.edu.cn/raspbian/raspbian/ jessie main contrib non-free rpi
```

华中科技大学开源镜像站：

```
deb http://mirrors.hust.edu.cn/raspbian/raspbian/ wheezy main non-free contrib
deb-src http://mirrors.hust.edu.cn/raspbian/raspbian/ wheezy main non-free contrib
```

阿里巴巴开源镜像站：

```
deb http://mirrors.aliyun.com/raspbian/raspbian/ wheezy main non-free contrib
deb-src http://mirrors.aliyun.com/raspbian/raspbian/ wheezy main non-free contrib
```


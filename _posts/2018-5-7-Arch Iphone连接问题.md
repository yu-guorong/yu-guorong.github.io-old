---
layout: post
title: Arch IPHONE连接问题
---

使用Arch时发现，iphone通过usb连接电脑，第一次连接时能够正常充电，在断开后再接线，就不能充电了，更换usb接口后可以正常充电。之前的usb口在电脑重启后才能继续充电。

通过`dmesg`发现一条输出`ipheth 1-12:4.2: Apple iPhone USB Ethernet now disconnected`

在查询`ipheth`的时候发现了论坛中的类似情况。[Problem connecting IPhone on USB](https://bbs.archlinux.org/viewtopic.php?id=229475)

#### 解决方法
![解决方法]({{ site.baseurl }}/images/2018-5-07/bbse1.png)

注释掉 `/lib/udev/rules.d/39-usbmuxd.rules`文件最后一行
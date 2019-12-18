---
layout: post
title: "修改工程名"
subtitle: "在Android Studio中给项目重命名"
author: "Jack Pan"
header-img:   "img/androidstudio/bg-androidstudio.jpg"
header-mask:  0.5
tags:
  - Android
  - Android Studio
---

## 在Android Studio 中修改工程名

### 使用场景

在Android Studio中一个现成的工程，因为某些原因，我们要修改工程名

- 举个例子

现有的工程名是: androidSamples,  需要改成 androidMultiSamples

## 尝试

- 直接在AS中refactor功能

![image-20191218173717986](/img/androidstudio/1.png)

- Rename后输入新名字

![image-20191218173801866](/img/androidstudio/2.png)

- Failed!!     此方法不可行。。



## 方案

### 目标

- 把工程名从 androidSamples -> androidMultiSamples

- applicationId 同步调整
- 包名路径同步调整

![image-20191218174147060](/img/androidstudio/3.png)

### 1.  删除一些配置文件

直接删除.idea文件夹   （删除后重新打开工程会新建）

### 2. 修改包名路径

![image-20191218174340828](/img/androidstudio/4.png)

- 选择rename

![image-20191218174533498](/img/androidstudio/5.png)

- 选择 refactor.

### 3. 修改 androidSamples.iml

- 修改 文件里  字段值为： androidMultiSamples

  ![image-20191218174730381](/img/androidstudio/6.png)

- 修改文件名为： androidMultiSamples.iml



### 4. 设置app/build.gradle   文件的applicationId 为： applicationId "com.jackpan.androidmultisamples"

![image-20191218174940823](/img/androidstudio/7.png)



### 5. 设置 settings.gradle文件： rootProject.name='androidMultiSamples'

![image-20191218175035710](/img/androidstudio/8.png)





### 6. AS关闭此项目，修改项目文件夹名字为： androidMultiSamples
![image-20191218174940823](/img/androidstudio/9.png)

### 7. 重新打开此项目
![image-20191218174940823](/img/androidstudio/10.png)
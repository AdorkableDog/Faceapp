# Faceapp人脸检测SDK集成说明文档
## 一、简介

Facepp人脸检测SDK是旷视科技推出的人脸检测工具包，提供快速，简洁的开发接口，支持Android4.2及以上的移动设备上实现人脸检测

### 功能特性
* 支持人脸的fast检测
* 支持人脸的robust检测
* 支持获取人脸关键点
* 支持人脸比对
* 支持获取人脸框
* 支持检测年龄性别
* 支持获取3dpose
* 支持 ARMv7a和ARM64v8a架构
* 支持Android 4.2及以上系统
* 快速，库文件小，贴合度高

### 组件及资源
FaceppSDK包含demo、sdk、docs三部分，[demo和sdk可以查看github](https://github.com/FacePlusPlus/MegviiFacepp-Android-SDK)

* demo部分：里面包含一个示例工程，实现了人脸检测的功能，有完整的源代码。
* sdk部分：里面包含了一套jni的封装，可以实现aar和c的两种集成方式。
* 库文件：人脸检测的实现库，路径以及目录如下sdk/src/main/jniLibs
├── armeabi-v7a
│   ├── libmegface-new .so
│   ├── libMegviiFacepp-0.5.2 .so
├── arm64-v8a
│   ├── libmegface-new .so
│   ├── libMegviiFacepp-0.5.2 .so
* 模型文件：人脸检测的训练模型，模型目前分在线授权和离线授权两种，路径/faceppdemo/src/main/res/raw/megviifacepp_0_5_2_model
> 试⽤版SDK有使用时间和使用次数的限制，如需正式版请通过[Face++官网](https://www.faceplusplus.com.cn)联系商务合作。

## 二、开发指南
### 阅读对象
本文档为技术文档，需要阅读者具有基本的Android开发能力，如果想对c定制开发需要有基本的c开发能力。

### 文档综述
FaceppSDK是适用android平台下的人脸检测SDK，提供aar，jar，c的三种接入方式，提供了简捷的接口方便接入。

### 开发准备

#### 在线授权的准备
1. [官网](https://www.faceplusplus.com.cn/)注册账号
2. 申请[key和secret](https://console.faceplusplus.com.cn/dashboard),用于在线授权。
3. 申请[Bundle ID（applicationId）](https://console.faceplusplus.com.cn/dashboard)，用于模型的验证。

 修改配置文件，使用者去开发者平台上申请对应的[ API_KEY , API_SECRET ]值，填写的Util文件中。


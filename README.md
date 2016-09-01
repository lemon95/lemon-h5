
Lemon Video Android SDK
============

## 简介
lib 目录包含一个 Library Project：`f_videoarr`。  
可以直接将两个 Library Project 作为依赖库，导入到你的项目。支持 Android Studio（建议）和 Eclipse。  
example 文件夹里面是一个简单的接入示例，该示例仅供参考。想使用该示例，请直接将本仓库导入。
img 目录中包含了接入后界面样式。

## 版本要求
Android SDK 要求 Android 4.0 及以上版本  
请使用 Java 7 或以上版本

## 接入方法
#### 1、联系柠檬运营申请相应的渠道key “LEMON_SECRETKEY” ，应用key “LEMON_APPKEY”；
#### 2、在自己的工程项目中引入Library Project:'f_videoarr' 并添加依赖；[引入DEMO](http://jingyan.baidu.com/article/1974b2898917aff4b1f77415.html)
#### 3、在Library Project：‘f_videoarr’ 的清单文件AndroidManifest.xml 中配置申请的渠道key和应用key
```xml
  <meta-data android:name="LEMON_SECRETKEY" android:value="渠道key" />
  <meta-data android:name="LEMON_APPKEY" android:value="应用key" />
```
#### 4、调用方法：
###### （1）、游客进入：
```java
Intent intent = new Intent(MainActivity.this, com.lemon95.lemonvideolib.MainActivity.class);
startActivity(intent);
```
###### （2）、带用户信息进入：
```java
Intent intent = new Intent(MainActivity.this, com.lemon95.lemonvideolib.MainActivity.class);
intent.putExtra("Mobile", "18500232066");  //手机号 必须
intent.putExtra("NickName", "maple");      //用户昵称 必须
intent.putExtra("HeadImgUrl", "http://b.hiphotos.baidu.com/zhidao/pic/item/dc54564e9258d1092a3090eed158ccbf6d814d9e.jpg"); //用户图像 非必需
startActivity(intent);
```
#### 5、启动效果
![](https://github.com/lemon95/lemon-android/img/1.gif "首页") ![](https://github.com/lemon95/lemon-android/img/2.gif "影视列表")

## 注意事项
* Lemon Video Android SDK 可能会与百度统计等其他第三方 jar 包冲突，当同时使用这些 jar 包的时候用户需要根据情况判断保留哪一方的 jar 包。
* 新版建议使用 Android Studio

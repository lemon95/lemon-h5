Lemon Video H5 SDK
============

## 简介
1、该接口提供渠道对接柠檬H5影视资源链接，对接方式有微信公众号对接或者App对接。</br>
2、该接口为柠檬影视渠道接口入口，分为两种形式，游客和登录用户，如果是游客则不需要填写手机号和昵称，如果是登录用户，则直接传人用户的手机号等信息。

## 准备工作
   联系柠檬运营申请相应的渠道key “SecretKey” ，应用key “AppKey”；

## 接口说明
 1、接口链接：http://ym.lemon95.com/lacel/index/auto?SecretKey=&AppKey=&Mobile=&NickName=&title=&color= </br>
 2、参数说明：

| 参数  | 说明 | 是否必须 | 举例 
| ---------- | -----------| -----------| -----------|
| SecretKey   | 渠道key   | 是 | ec8b570ad4bd403783c52ecb5cdfa849
| AppKey   | 应用key   |  是 |1259402909 
| Mobile   | 用户手机号   | 否（默认游客）|
| NickName  | 用户昵称   | 否 （默认游客）|
| title  | 影视标题  | 否 （默认‘影檬’）| 测试影院 建议URLEncoder.encode("", "UTF-8"); 编码
| color  | 界面主题颜色   | 否  （默认‘蓝色’）| 33cd5f
 [测试链接（http://ym.lemon95.com/lacel/index/auto?SecretKey=ec8b570ad4bd403783c52ecb5cdfa849&AppKey=1259402909&Mobile=&NickName=&title=测试影院&color=33cd5f）](http://ym.lemon95.com/lacel/index/auto?SecretKey=ec8b570ad4bd403783c52ecb5cdfa849&AppKey=1259402909&Mobile=&NickName=&title=测试影院&color=33cd5f)

## 注意事项
* App接入时由于Android 原生WebView对H5视频支持不是很好，部分手机没法全屏，下面提供2种解决方法：</br>
1、参考上面文件夹 ‘解决Android App接入视频不能全屏DEMO’ </br>
2、采用腾讯X5内核 [http://x5.tencent.com/doc?id=1004](http://x5.tencent.com/doc?id=1004) ,用户在app是浏览体验和在微信上相同。
* 新版建议使用腾讯X5内核

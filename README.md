# WxPayAPI 微信支付的例子，包括原生app、公众号、h5等

## 微信js sdk
   微信JS-SDK是微信公众平台面向**网页开发者**提供的基于微信内的网页开发工具包，必须在微信安卓、IOS版本的内置浏览器使用
   微信JS-SDK是微信公众平台面向网页开发者提供的基于微信内的网页开发工具包（Software Development Kit）
   
微信JS-SDK主要包含以下能力：

1、分享类接口
支持获取“分享到朋友圈”、“发送给朋友”、“分享到QQ”和“分享到微博”按钮的用户点击状态，同时支持自定义分享内容。

2、图像类接口
支持拍照、从手机相册选择图片、上传图片、下载图片、预览图片功能。

3、音频类接口
支持实现录制、播放、暂停播放语音等功能，同时支持将语音快速上传到云端服务器或从云端服务器将语音快速下载到网页。

4、智能类接口
支持将语音快速地转换成文字。开发者无需掌握语音识别相关技术，只需简单地引用微信JS-SDK提供的方法即可实现。

5、设备信息类接口
支持获取当前手机设备的网络状态，如2g、3g、4g或wifi，为用户提供流畅的浏览体验。

6、地理位置类接口
支持获取用户的地理位置信息（需用户同意），支持使用微信内置的地图查看器查看地理位置或导航。

7、界面操作类接口
支持隐藏或显示微信内置浏览器“右上角菜单”、“分享到朋友圈”、“发送给朋友”、“复制链接”等指定的按钮，支持关闭当前网页窗口以返回公众号会话。

8、微信扫一扫接口
支持使用微信扫一扫，扫描一维码或二维码，并将用户扫码内容交由微信处理或返回给网页由网页处理。

9、微信小店接口
支持从网页跳转到指定的微信小店商品页，商品页支持浏览商品的详细信息，支持完整的购买、客服等流程。

10、微信卡券接口
支持添加卡券、查看卡券及调起卡券列表等功能。

11、微信支付接口
支持有支付权限的公众号在网页发起一个微信支付请求。

## 微信支付接口 包括H5（wap）、原生APP、公众号、小程序等[详细这里](https://pay.weixin.qq.com/wiki/doc/api/index.html)

小程序支付API接口[详细这里](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=9_1)

小程序支付的交互图![如下](https://pay.weixin.qq.com/wiki/doc/api/img/wxa-7-2.jpg)

商户系统和微信支付系统主要交互：

1. 小程序内调用登录接口，获取到用户的openid,api参见公共api[小程序登录API](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/login/wx.login.html)

2. 商户server调用支付统一下单，api参见公共api[统一下单API](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=9_1&index=1)

3. 商户server调用再次签名，api参见公共api[再次签名](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_7&index=3)

4. 商户server接收支付通知，api参见公共api[支付结果通知API](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=9_7)

5. 商户server查询支付结果，api参见公共api[查询订单API](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=9_2)

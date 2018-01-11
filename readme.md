# TVRemoteIME 
电视盒子的远程输入法应用，可跨屏远程输入和跨屏远程控制盒子 
# 安装方法
## 一、通过adb命令安装应用  
1、电视盒子开启adb调试 

2、电脑通过adb命令连接电视盒子（假如电视盒子的内网ip为：192.168.1.100）  
`adb connect 192.168.1.100:5555`  
注意,手机要与盒子在同一个WIFI网络(内网网络)  执行`adb devices`命令显示有device列表，则表示已连接上盒子，可继续下一步

3、通过以下命令安装输入法apk包  
`adb install IMEService-release.apk`  

4、设置为系统默认输入法  
`adb shell ime set com.android.tvremoteime/.IMEService`  

5、电脑或者手机访问远程输入法的控制页面
`http://192.168.1.100:9978/`  

## 二、通过U盘或者其它方式安装  
1、安装后在盒子应用列表里找到TVRemoteIME的图标点击运行  

2、根据应用的提示进行设置即可。  

## 控制界面示例截图  
注： 输入控制端不需要安装任何APK应用，直接浏览器操作  

![示例截图](https://raw.githubusercontent.com/kingthy/TVRemoteIME/master/released/screenshot.jpg "控制界面示例截图")  

# 引用第三方包/资源说明
1、[NanoHttpd](https://github.com/NanoHttpd/nanohttpd "NanoHttpd")  用于实现HTTP WEB服务  

2、[ZXing](https://github.com/zxing/zxing/ "QRCode") 用于实现二维码的输出
 
3、[悟空遥控](http://www.wukongtv.com/views/input.html "悟空遥控")  非常棒的一款遥控软件。  
注：本软件远程控制端的遥控导航面板设计图和小部分CSS代码参考于它。

# TVRemoteIME 
电视盒子的远程输入法应用，可跨屏远程输入和跨屏远程控制盒子 
# 安装方法
## 通过adb命令安装应用  
1、电视盒子开启adb调试  

2、电脑通过adb命令连接电视盒子（假如电视盒子的内网ip为：192.168.1.100）  
~adb connect 192.168.1.100:5555  ~
注意,手机要与盒子在同一个WIFI网络(内网网络)  执行~adb devices~命令显示有device列表，则表示已连接上盒子，可继续下一步

3、通过以下命令安装输入法apk包  
~adb install IMEService-release.apk~  

4、设置为系统默认输入法  
~adb shell ime set com.android.tvremoteime/.IMEService~  

5、电脑或者手机访问远程输入法的控制页面
~http://192.168.1.100:9978/~  

## 通过U盘或者其它方式安装  
1、安装后在盒子应用列表里找到TVRemoteIME的图标点击运行  

2、根据应用的提示进行设置即可。  
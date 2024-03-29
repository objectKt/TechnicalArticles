```
adb 常用命令

1、显示系统中全部设备：
adb devices

List of devices attached
emulator-5554 device

2、开启ADB服务：
adb start-server

3、关闭ADB服务：
adb kill-server

4、连接设备
adb connect 192.168.1.61

5.断开设备：
adb disconnect 192.168.1.61

6、、安装apk
adb install xx.apk

7、列出手机装的所有app的包名：
adb shell pm list packages

列出系统应用的所有包名：
adb shell pm list packages -s

列出除了系统应用的第三方应用包名：
adb shell pm list packages -

8、卸载已安装的应用
adb uninstall com.tencent.mm

success

9、清除应用数据与缓存：
adb shell pm clear com.tencent.mm

10.强制停止应用
adb shell am force-stop com.tencent.mm
```

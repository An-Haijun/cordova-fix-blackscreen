cordova生成的android应用，启动前，会因为默认的黑色或白色背景，出现闪一下的黑白屏，为了解决这个问题，添加一个默认的背景图，同时screen.png作为cordova默认的启动屏图片，于是背景图设为screen.png
#使用方法
步骤1——安装本插件：
```
cordova plugin add 本插件路径
 ```
步骤2——安装[cordova-custom-config](https://github.com/dpa99c/cordova-custom-config):
```
cordova plugin add cordova-custom-config
 ```
应用项目的config.xml文件添加一句：
 ```android
 <edit-config file="app/src/main/AndroidManifest.xml" mode="merge" target="/manifest/application/activity[@android:name='MainActivity']" xmlns:android="http://schemas.android.com/apk/res/android">
     <activity android:theme="@style/WelcomeStyle" />
 </edit-config>
 ```
这样就大功告成了！

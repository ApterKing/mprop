# mprop
Android开启调试的工具mprop

## 使用方法

根据手机架构拷贝对应的mprop到/data/local/tmp/目录

```
adb push [mprop路径] /data/local/tmp/
```

进入adb shell

```
adb shell
su
cd /data/local/tmp/
chmod 755 mprop
```

执行mprop设置debuggable=1

```
/data/local/tmp/mprop
setprop ro.debuggable 1
/data/local/tmp/mprop -r
getprop ro.debuggable #查看当前属性
```

最后需要重启adb，重启Android Studio

```
adb kill-server
```

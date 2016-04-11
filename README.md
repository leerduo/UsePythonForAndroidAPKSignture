# UsePythonForAndroidAPKSignture
使用Python给apk包签名 原文链接:http://mushuichuan.com/2016/03/23/python-sign/
```java

import os

path="C:\EnHancement\\" #改为你存放apk包和keystore的目录
v = raw_input("Please input version:")
cmd = "jarsigner -digestalg SHA1 -sigalg MD5withRSA -verbose -keystore %sandroidkey.keystore -signedjar signed%s.apk %sunSigned.apk carsmart" %(path,v,path)
os.system(cmd)
#防止程序运行完后直接关闭
raw_input()
```

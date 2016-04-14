#谷歌地图有签名验证，于是重新签名后地图会不能显示


# 简单的方法 #

从上面的 Downloads 中下载 tieba\_helper\_modified.key 用这个key来做签名。

这个key的别名是：tieba\_helper\_modified，密码是：tiebahelper


在签名前，修改 AndroidManifest.xml 中这个：
```
<meta-data android:name="com.google.android.maps.v2.API_KEY" android:value="AIzaSyDKzKuCkQBs0KfygAf_QAiqqTXiYVk8hto"/>
```

改value的值。

如果是覆盖版，value值修改成：AIzaSyCDvqFQc\_X4UdzNAWSslLl\_dZXJqJxWhz0


如果是兼容版，value值修改成：AIzaSyBu43JnTrgz4Vzf\_EXW1U7GMLeknubNzwM


如果是共存版，由于package名称变了，看下面的方法。


# 麻烦点的方法，但可以用自己的签名key #

原理就是乃自己去申请一个 google map v2 for android 的key，然后根据自己的签名文件填写上面的那个value值即可。

方法：https://developers.google.com/maps/documentation/android/start?hl=zh-cn 跟着 “Getting the Google Maps Android API v2” 做即可。


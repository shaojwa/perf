#### 测试硬盘性能
```
hdparm -Tt /dev/sda
```

#### 测试硬盘缓存
```
hdparm -I /dev/sda
```
注意是大写的`I`，在Configuration项下面有：`cache/buffer size = unknown`, -I是比-i显示更为详细的扩展格式信息。

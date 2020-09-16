蓝湖里给的色域是sRGB，xib默认为 
```
colorSpace="calibratedRGB"
```
此脚本修改为：
```
colorSpace="custom" customColorSpace="sRGB"
```

代码里的QMUI用的也是sRGB，这样就可以统一了



使用方法：
1、将bin/rgb复制到/usr/local/bin/目录下 (cp ./bin/rgb /usr/local/bin/rgb)
2、设置权限 (sudo chmod 777 /usr/local/bin/rgb)
3、使用时，cd 到工程目录，再执行 rgb 即可

注意不要手动修改xib中的色域，否则脚本不起效果


进一步：
1、可以将命令放入githooks中，每次提交都自动执行。
2、可以将命令放入jenkins shell中，这样每次打包都会去执行（只是调试的时候看起来不一致）。

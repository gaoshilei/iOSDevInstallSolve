1.  安装 macports (安装过程需要连接VPN,否则无法安装成功)

2.  安装完MacPorts后打开终端，输入 sudo port -v selfupdate 更新MacPorts到最新版本，时间可能比较长。

3.  更新完MacPorts后安装DPKG文件，在终端输入sudo port -f install dpkg

4.  下载安装 iosopendev 如果安装失败，可以通过 Command + L 查看安装中出现的问题。
```
PackageKit: Install Failed: Error Domain=PKInstallErrorDomain Code=112 "运行软件包“iOSOpenDev-1.6-2.pkg”的脚本时出错。" UserInfo={NSFilePath=./postinstall, NSURL=file://localhost/Users/ice/Downloads/iOSOpenDev-1.6-2.pkg#iodsetup.pkg, PKInstallPackageIdentifier=com.iosopendev.iosopendev162.iod-setup.pkg, NSLocalizedDescription=运行软件包“iOSOpenDev-1.6-2.pkg”的脚本时出错。} {
NSFilePath = "./postinstall";
NSLocalizedDescription = "\U8fd0\U884c\U8f6f\U4ef6\U5305\U201ciOSOpenDev-1.6-2.pkg\U201d\U7684\U811a\U672c\U65f6\U51fa\U9519\U3002";
NSURL = "file://localhost/Users/ice/Downloads/iOSOpenDev-1.6-2.pkg#iodsetup.pkg";
PKInstallPackageIdentifier = "com.iosopendev.iosopendev162.iod-setup.pkg";
}
```  
5.  修复安装失败问题  
打开步骤4下载的Specifications文件夹，里面应该有8个文件,如果你有安装多个xcode注意放到对应的xcode里面。  
>   （1）iPhoneOS开头的四个文件放到/应用程序/Xcode/Content/Developer/Platforms/IphoneOS.platform/Developer/Library/Xcode/Specifications文件夹下（如果没有，请自己创建一个）  
（2）iPhone Simulator 开头的另外四个文件放入/应用程序/Xcode/Content/Developer/Platforms/iPhoneSimulator.platform/Developer/Library/Xcode/Specifications文件夹下(如果没有，请同样创建一个)  
（3）在/应用程序/Xcode/Content/Developer/Platforms/iPhoneSimulator.platform/Developer/文件夹下创建usr文件夹，usr文件夹下再创建一个名为bin的文件夹

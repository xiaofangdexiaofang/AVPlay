# AVPlay
音视频播放Demo

### Utils文件夹主要是工具类
* Player 是之前自定义的Demo，包括下载和播放  
* HTTPServer 是M3U8的本地播放的三方库  
* CustomRefresh 是首页自定义头部刷新

### NetWork是网络请求部分
* Request 是请求基类

### Category文件夹是分类
* NSString+Extension NSString+Size 根据字数计算长宽度 
* UIColor+ColorTool 颜色的分类

### Resource存放资源
* 添加主页下拉刷新动画以及音乐播放浮窗的动画，主要根据UIScrollView的偏移量判断显示与否，动画采用lottie-ios

### Vender是放置本地三方库
* ZFPlayer 视频播放类 
* IJKMediaFrameWork 是编译好的三方类库 
* MBProgressHUD+NJ 是自定义的加载类库 
* NullSafe 基于Runtime的类库，防止Map找不到key而闪退

### Modules 
* Home 主页面
* 主要是界面搭建以及视频播放和音频的播放，下拉动画实现，视频小窗口播放。
* 音频主要是使用FreeStreamer播放，目前主要是mp3格式，后续会测试其他格式。音乐浮窗动画的实现以及锁屏的播放和暂停，目前上一首和下一首暂无实现，接口已预留。这边在开发锁屏界面的时候，需要注意添加当前已播放时间，否则每次暂停，进度条都会从0开始。
* 视频的投屏是使用MRDLNA这个三方库，目前只支持DLNA这个协议，后续出现其他投屏失败问题，再根据协议增加解决的办法。
* 添加LBLelinkKit三方库，目前已将代码集成进去，但是资质还在审核中，没有APPSecret和APPId，暂时无法测试。已打客服电话催审核进度。
* 投屏使用的是乐播的SDK，看文档，遵循相关的协议以及代理方法即可实现，注意点：目前SDK中支持三种协议，主要使用的是乐联协议和DNLA协议，处于同一个网段，连接的乐联协议，处于非局域网，连接的是DNLA协议
Guide 引导页

### Root 存放Controller的基类
### AppDelegate 存放主入口以及资源文件，pch文件以及plist文件
* 音乐的锁屏以及引导页的相关的代码设置已添加到AppDelegate文件

### Pods 主要是网络三方库
 * pod 'Masonry', '~> 1.1.0'
 * pod 'LCTabBarController', '~> 1.3.7'
 * pod 'AFNetworking', '~> 3.2.1'
 * pod 'MBProgressHUD'
 * pod 'SDWebImage', '~> 5.0.0-beta5'
 * pod 'DZNEmptyDataSet', '~> 1.8.1'
 * pod 'IQKeyboardManager', '~> 6.3.0'
 * pod 'WRNavigationBar', '~> 1.2.0'
 * pod 'CocoaAsyncSocket', '~> 7.6.3'
 * pod 'SocketRocket'
 * pod 'UITableView+FDTemplateLayoutCell'
 * pod 'MJExtension'
 * pod 'MJRefresh'
 * pod 'CDNByeSDK'
 * pod 'lottie-ios', '~> 2.5.0'
 * pod 'CocoaHTTPServer'
 * pod 'M3U8Kit'
 * pod 'FreeStreamer', '~> 3.8.0’
 * pod 'MRDLNA'
 * pod 'LBLelinkKit'
 * pod 'DoraemonKit/Core', '~> 1.1.9', :configurations => ['Debug']
 * pod 'DoraemonKit/WithLogger', '~> 1.1.9', :configurations => ['Debug']

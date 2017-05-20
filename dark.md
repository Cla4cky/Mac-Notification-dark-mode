#mac通知中心修改背景颜色为暗色
##提示：这个办法目前对macOS Sierra系统 10.12.4版本还有效果，10.12.25 beta我还没去测试，一般只要版本不要太低都能使用这个办法来修改的。
- 首先我们先去关闭我们的通知中心，在terminal里面输入一下命令：
launchctl unload -w /System/Library/LaunchAgents/com.apple.notificationcenterui.plist。
- 然后我们去<a href="http://fox.furcode.co/macos/DarkNotificationCenter-foxlet.zip" title="补丁">补丁</a>这下载我们暗色背景的补丁，下载好了后，我们解压下zip会发现有2个文件。
- 2个文件分别是NotificationCenter.framework和NotificationCenter.app。我们需要把这里得到的2个补丁替换掉我们系统自带的，NotificationCenter.app在系统里的路径是：/System/Library/CoreServices/NotificationCenter.app。NotificationCenter.framework的是/System/Library/Frameworks/NotificationCenter.framework。替换前最好先把系统自带的复制一个到别的文件夹里面做备份，如果修改有问题还能及时改回来！
- 替换了文件后，我们需要重新启动下我们的mac，等mac重新启动好了后，我们再去terminal里面输入以下命令：launchctl load -w /System/Library/LaunchAgents/com.apple.notificationcenterui.plist。然后我们再度重新启动我们的mac。
- 等mac启动好了后我们去看看我们的通知中心那，是不是就是黑色的了，而且还有点微特效加了进去，目前没发现有任何不兼容的问题。

#这里感谢macrumors作者foxlet提供的补丁！ENDS！

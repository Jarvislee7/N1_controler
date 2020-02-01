# n1遥控器使用说明

自己给斐讯的N1的盒子刷了YYF的电视盒子系统后，发现没有合适的遥控器，目前网上提供的遥控器有的不能完全适配，有的有很多广告弹出来，所以查看了遥控器的实现原理发现就是简单的局域网内的api调用，所以动手实现了这个app,提供给大家使用，界面是自己参照遥控器设置的，如果哪里使用不爽或者有问题欢迎提出ISSUE我会尽快修改。

### 下载地址：https://fir.im/n1Controller

### app界面截图：

![controller.png](https://i.loli.net/2020/02/01/8Zzf6aTSr1MAWiv.png)

- 首次使用前请先查看你的盒子的IP地址，例如我的是192.168.168.113，在界面的右上方点击IP按钮,输入即可，当盒子连接的网络发生变化的时候需要及时更换确保遥控器生效
- 确保手机wifi和盒子处在同一个网络中，才能使遥控器生效
- 卸载或者清除缓存后请重新设置ip地址
- 该app无法实现n1开机，但是可以关机，因为我从不关机我也不是很关心这个，可以买个智能插座进行开机控制。


### 接口说明

URL:http://N1的IP:8080/v1/keyevent  (发送按钮指令)
方式：POST
参数内容：

{"keycode":按键代码,"longclick":false}
按键代码列表：

- 上:19
- 下:20
- 左:21
- 右:22
- 返回:4
- 音量加:24
- 音量减:25
- 主界面:3
- 菜单:82
- 确认键:23
- 电源:26

URL: http://N1的IP:8080/v1/action (打开设置界面)
方式：POS
参数内容：

{"action":"setting"}


祝大家使用的开心
---
title: 'ShadowsocksR 发布 C# v3.4.0'
date: '2015-08-25 23:27:48'
updated: '2015-09-20 21:28:40'
categories: 日常
tags:
  - shadowsocks
---


昨天的 commit，看来 @breakwa11 是要接下这个坑呢。祝好。

[https://github.com/breakwa11/shadowsocks-rss](https://github.com/breakwa11/shadowsocks-rss)

- - - - - -

是的，你发现了我之前说的“最后一个版本”出尔反尔了，我就是这么说话不算话，包括之前说的闭源一年的话（或者我就一开始就开源了，谁知道呢）。你 喜欢我说话不算话还是说到做到呢？相对于现在大家的处境（以及我的处境）来说，个人认为这些都不是什么大问题。我还是会顺着 clowwindy 的意思做的。

本版本发布其中一个实验性功能：TCP over UDP。但是**这个功能目前有BUG，将来也极可能不兼容**，功能在实现时预留了巨大的改进空间，可能要经历较长的修改稳定时间，此版本只实现了最最基本的功能，目前仅为可用的状态。但此功能对地区特别敏感，因为使用UDP发送数据包，部分地区存在*因大量UDP流量而临时性封锁IP端口*的 策略，请谨慎使用。目前具体实现协议的说明可以参阅源码中的注释。（我比较菜，当时写这个东西写了好长时间，这也是之前不想开源的主要原因之一，你不可能 提前告诉墙国人民说，“看，我要写这个这个这个，有本事在推出前就把协议封锁掉吧”。再另外，这个东西要是用的人一多，UDP 通讯必定会被人为恶化，到时 候又会有人说因为 SSR 导致 UDP 变差了，游戏玩不了了。但不发的话，别人只看到界面上的变化，以为 SSR 啥都没做。那我到底要不要发这个实验功能？事实 上这个功能在 3.3.2 版之后已经使用隐蔽的方式小范围发布给一些站长进行测试，如今只是把这个实验性功能明着放出来。

另外，除了要感谢 clowwindy，还要感谢“编程随想”，以及所有参与的开发者们。




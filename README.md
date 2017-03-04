ngrokc LuCI for OpenWrt/LEDE 
===
forked from https://github.com/anti-gfw/packages/tree/master/luci/applications/luci-app-ngrok

为ImageBuilder编译[此固件][N]所需依赖包而建，非原创

简介
---

 软件包为ngrok-c的luci配置页面,可配合[openwrt-ngrokc][M]使用
 
 支持HTTP和TCP两种模式的内网穿透
 
依赖
---
显式依赖 `ngrokc`

编译
---

 - 从 OpenWrt 的 [SDK][S] 编译  

   ```bash
   # 以 ar71xx 平台为例
   tar xjf OpenWrt-SDK-ar71xx-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
   cd OpenWrt-SDK-ar71xx-*
   # 获取 Makefile
   git clone https://github.com/AlexZhuo/luci-app-ngrokc.git package/luci-app-ngrokc
   # 选择要编译的包 Network -> Luci -> luci-app-ngrokc
   make menuconfig
   # 开始编译
   make package/luci-app-ngrokc/compile V=99
   ```

---

截图
---
![](https://github.com/AlexZhuo/BreakwallOpenWrt/raw/master/screenshots/ngrokc1.png)


![](https://github.com/AlexZhuo/BreakwallOpenWrt/raw/master/screenshots/ngrokc2.png)

[N]: http://www.right.com.cn/forum/thread-198649-1-1.html
[M]: https://github.com/AlexZhuo/openwrt-ngrokc
[S]: http://wiki.openwrt.org/doc/howto/obtain.firmware.sdk

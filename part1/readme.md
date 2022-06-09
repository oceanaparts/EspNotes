# 1.ESP32介绍及资料查找

 Esp32相比STM32等芯片它的优势在于价格更为低廉并且具有联网功能，在编译上他没有像STM32有MDK5这样的IDE进行编译，需要自行进行一个工具链的配置，乐鑫官方推出的工具链框架为ESP-IDF，实际上MDK相当于把一套完整的编译，调试工具链都配置好，并集成在一个IDE中，而我们没有这样的开发环境因此只能手动配置好这一系列工具。
 在芯片类型上有ESP8266,ESP32,ESP32-C,ESP32-S，C系列性能有所阉割但是价格更为低廉，S系列待学习。而我们日常所提到的ESP32-CAM实际上是基于ESP32的一款支持相机的模组，这里就提到了一个概念--**模组**

>**模组：** 由于ESP32是一款物联网芯片，在硬件上需要有天线电路，绘制得不好会导致信号出现问题，模组相当于一个最小系统板，官方对每一款芯片都设计了不止一个模组以适配不同的应用场景。

>**开发板：** 官方也设计了许多开发板，下游厂商也有设计，比如我后续使用的合宙的ESP32C3开发板

<div align=center><img src="https://s2.loli.net/2022/06/09/RUEZkNsOaqgIw91.png"></div>

>**开发环境** 上，我们可以选择的语言有C,MicroPython,Lua;
框架有ESP-IDF(C),ARDUINO(C),micropython,Lua等;ESP-IDF更接近底层且功能更强大。
IDE有：VS Code+ESP-IDF插件，VS Code+Platform插件(支持ESP-IDF与ARDUINO)，官方的ESP Eclipse(ESP-IDF框架)，以及使用Lua开发时使用合宙的VS Code+LuatOS-SOC推荐拓展包插件,Thonny(micropython)

**后续主要使用VS Code+ESP-IDF插件使用C语言开发**

[MicroPython](http://www.micropython.org/)与Lua语言都需要往芯片烧录**解释器固件**
MicroPython固件[下载链接](http://www.micropython.org/download/),[烧录教程](https://www.bilibili.com/read/cv15460009/)，IDE使用Eclipse，可借鉴[教程]
Lua烧录与使用见[合宙文档](https://wiki.luatos.com/boardGuide/index.html)

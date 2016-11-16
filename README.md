# androidNotes
* 1.由来
   最初由安迪·鲁宾研发，于2005年被谷歌收购，android名字来源于安迪小时候所玩的一款游戏的人物名，图标由设计师看见厕所图标所获得的灵感
* android2.3开始支持NFC(进场通信技术),android3.0开始支持平板,4.1.2是4.0之后比较稳定的版本
* android架构：分层架构
```
  1.application,home contacts,phone ,..
  2.application framework(用java开发+ JNI), activity Manager(管理应用),view system（展示视图），window manager（对话框管理),content providers(内容提供者)，package manager(包管理),telephony manager ,resource manager ,locaiton manager,notification manager.
  3.libaries和dalvik虚拟机层,主要是c和c++开发的函数库，由于java不能直接调用c，所以2，3层之间有一个JNI(java native interfaceJAVA本地接口语言)
  4.linux kernel内核,主要是与硬件有关的驱动,用c语言开发
```
* 2.两种虚拟机的不同
```
   JVM:java虚拟机,执行多个.class文件，打包后问.jar,基于栈的架构， 栈是内存的一部分，执行的时候需要CPU寻址
   dvm:dalvik虚拟机，执行一个.dex,基于寄存器架构，是cpu的一部分，无需寻址执行，更快
```
* ART模式：android runtime简称，安装的时候免去了dalvik模式转换机器吗时间，直接将代码转换为机器码，好处：程序运行时，无需时时转换，运行速度快，缺点：安装时间长，占用内存大

8.4


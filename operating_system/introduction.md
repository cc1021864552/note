# 操作系统概论

## 一、操作系统是什么

​	OS是最底层的一个软件，这个软件可以访问、使用、控制和管理硬件设备，这个软件也可以调用、管理其他的"软件"。



## 二、为什么使用操作系统

​	计算机变得越来越复杂，如果让用户直接面对硬件，会给用户使用计算机增加很大的难度，而且没必要。通过使用操作系统，让用户眼里的计算机变得更加易于使用。



## 三、操作系统的功能

​	计算机是一种工具，用户利用他达到自己的目的，因此，理论上，计算机必须在能力范围之内帮助用户达到自己的目的，并尽量高效。

​	用户利用计算机达到自己目的的手段是使用程序，不管是自己编写的还是他人提供的，每个用户的目的不同，因此计算机上有各式各样的程序，这些程序存储在硬盘上，当我们使用这些程序时，他们便加载进内存，变成了进程，但CPU一次只能处理一个进程（部分），该处理哪个呢？这涉及到**进程的调度**的问题。两个进程之间可能不完全独立，有时他们需要协作，共同完成一个功能，那他们之间是如何沟通的呢？这涉及**进程间通信**的问题。

​	上面说了，程序和进程的区别在于，进程是将程序加载进内存后形成的。我们知道，程序是一个二进制序列，那进程"长"什么样呢？这涉及**进程结构的设计**。内存是一个容器，里面有许多的进程，这些进程在内存中是如何放置的呢？这涉及**内存的分配**。

​	当程序未被使用时，他们存储在硬盘上，但在用户眼中，硬盘是不存在的，取而代之的是文件系统。这是怎么做到的呢？这涉及**文件系统的设计和实现**。我们平时会对文件进行增删查改的操作，计算机是如何实现这些功能的呢？这涉及**文件系统的管理**。

​	计算机只是命令的执行者，用户才是命令的使用者，计算机是如何获取用户的指令的呢？通过I/O设备，如键盘、显示器、鼠标等。世界上这些设备的种类千千万，计算机都能一一识别吗？并不能。但计算机还是可以识别很多的设备的，怎么做到的呢？制定规则。只有当你的设备符合我的标准时，我才认识你。这涉及**I/O接口的适配**。当计算机连上了一个外设，他们之间是如何进行沟通和数据的传输的呢？这涉及**主机和I/O设备之间的通信**。

​	由上述可知，计算机帮助我们解决问题的过程可能会很复杂，但我们平时在使用计算机时，这些问题可能并不那么突出，是谁帮我们解决了这些问题呢？**Operating System**。



## 四、一个问题

两个个硬盘上的程序是如何进入内存，然后交替被CPU执行，完成各自功能的？

- 程序在硬盘上的存在形式；
- 程序进入内存变成进程；
- 进程被CPU执行；
- 进程调度；
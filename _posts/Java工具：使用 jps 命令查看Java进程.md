---
tags:
  - publish
---

作为 Java 开发人员，Java 虚拟机的常用性能分析的工具是必须要掌握的，JDK绑定的工具有7个，我会分7篇文章来介绍，本篇文章主要介绍 jps 命令。

## jps 是什么

jps 的全程是 java virtual machine process status tool，Java虚拟机自带的用来查看 Java 进程状态的命令行工具，它类似于 linux 下的 ps 命令，只不过它只列出与 Java 进程。使用这个工具可以查看 Java 进程ID和主类名称等信息。

## 使用 jps 命令

1、查看 Java 进程列表
```bash
$ jps
13089 JavaApp
17366 Jps
```

2、输出更详细的信息
```bash
$ jps -l 
17515 org.artifactId.MyApp 
13089 com.app.JavaApp 
17366 sun.tools.jps.Jps
```
3、输出虚拟机参数
```bash 
$ jps -m  
17515 MyApp -Xmx256m  
13089 JavaApp -Xms64m -Xmx512m
```

**更多的参数和说明如下：**

```
jps ：列出Java程序进程ID和Main函数名称 
jps -q ：只输出进程ID 
jps -m ：输出传递给Java进程（主函数）的参数 
jps -l ：输出主函数的完整路径 
jps -v ：显示传递给Java虚拟的参数
```
## 总结
jps非常简单，但是对于日常开发和运维却是非常重要，是必须要掌握的。

> 感谢阅读，祝您编码愉快！

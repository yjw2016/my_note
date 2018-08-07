[TOC]



# Golang

panic 中止  
recover 恢复  
一般而言，panic发生时，程序中断。并立即执行当前所处goroutine中被 延迟的defer函数。
而后，程序崩溃并输出日志信息（包括panic value及函数调用的堆栈跟踪信息）快捷键

## 并发

并行: parallel 多条指令在多个处理器上同时执行

并发: 多条指令高频轮换执行

```go
//     runtime 包
/*Gosched yields the processor, allowing other goroutines to run. It does not
 suspend the current goroutine, so execution resumes automatically.*/ 
//	无法控制时间长短，很难用
runtime.Gosched() 	
/*Goexit终止调用它的go程。其它go程不会受影响。Goexit会在终止该go程前执行所有defer的函数。
在程序的main go程调用本函数，会终结该go程，而不会让main返回。因为main函数没有回，程序会继续执行其它的go程。如果所有其它go程都退出了，程序就会崩溃。*/ 
runtime.Goexit()
/*
GOMAXPROCS设置可同时执行的最大CPU数，并返回先前的设置。 若 n < 1，它就不会更改当前设置。本地机器的逻辑CPU数可通过 NumCPU 查询。本函数在调度程序优化后会去掉。
*/
func GOMAXPROCS(n int) int
```



b

## 网络

## IO



-----------







# 附录

## 常用快捷键

### Typora
cmd  /  显示源码

### IDEA

V   cmd  alt  ：variable(自动赋值)

### Atom
shift cmd p 命令行
shift ctr m 显示preview   
ctr \ 显示目录



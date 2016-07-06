C/C++ 编程问题汇总
----
[<< 回到根目录]
## 1. 如何将整形变量转化为字符串变量，主要用于循环中输出文件时文件名含循环变量，提高结果的可读性？

思路，定义两个`char`数组，一个存有意义的文件名(e.g. time),另一个用来存储数字转换为的字符串，最后的
文件名为这两个字符数组拼接后的结果。

例如：

       str1 = "time";
       str2 = "128";
       str = "time128.txt";

实现过程，需要使用C的两个库函数`strcpy`, `strcat`,另外，还需要一个[`itoa`函数](https://github.com/nicklinyi/BasicCodes/blob/master/C/itoa.c)用于整形变量向字符串的转
化。

一个简单的例子如下：
  
         char str[100];
         char str2[20];
         int i;
         FILE *fp;
         for(i=0; i<100; ++i){
           strcpy(str,"time");
           itoa(i+1,str2,10);
           strcat(str,str2);
           strcat(str,".txt);
           fp = fopen(str,"w+");
         }

[<< 回到根目录]: ./README.md

Latex 问题汇总
=====
[回到根目录](./README.md)
##1. 公式里边的空格问题
链接：[http://blog.sina.com.cn/s/blog_4ddef8f80100iwwv.html](http://blog.sina.com.cn/s/blog_4ddef8f80100iwwv.html)

##2. 积分、双重积分、多重积分
- ![equation](http://latex.codecogs.com/gif.latex?\\int)  积分： `$\int$`
- ![equation](http://latex.codecogs.com/gif.latex?\\iint)  双重积分： `$\iint$`
- ![equation](http://latex.codecogs.com/gif.latex?\\iiint)  三重积分： `$\iiint$`
- ![equation](http://latex.codecogs.com/gif.latex?\\idotsint)  多重积分： `$\idotsint$`

参考资料：

\[1\]:《LaTeX入门》刘海洋，245页

\[2\]:  [博文](http://trumanliu.com/github-markdown-math-formulas/)

##3. 公式关系符对齐

例子：

![equation](http://latex.codecogs.com/gif.latex?\\begin{align*}
   & p(t,x) \\notag \\\\
={}& \\int e^{ik_{x}x}[\\int e^{-i\\omega t}P(\\omega,k_{x})d\\omega]dk_{x} \\notag \\\\
={}& \\int e^{ik_{x}x}P(t,k_{x})dk_{x} \\notag
\\end{align*}) 

代码：
```
   \begin{align*}
      & p(t,x) \notag \\
   ={}& \int e^{ik_{x}x}[\int e^{-i\omega t}P(\omega,k_{x})d\omega]dk_{x} \notag \\
   ={}& \int e^{ik_{x}x}P(t,k_{x})dk_{x} \notag
   \end{align*}
```
参考资料：

\[1\]:《LaTeX入门》刘海洋，265页

##4. 多行公式，前几行不标记，最后一行标记
对于这种情况，可采用`gather`环境
例如:

	\begin{gather}
	R_{\infty}=1-\frac{X^2}{1+R_{\infty}} \notag \\
	R_{\infty}(1+R_{\infty})=1+R_{\infty}-X^2 \notag \\
	R^2=1-X^2
	\end{gather}
最终的显示如下：
![](http://i.imgur.com/N7Exn4B.png)
参考资料：
\[1\]:《LaTeX入门》刘海洋，264页

##5. 注意事项
在表格中，`\label`语句应放在表格语句范围内靠后的位置，不然`\ref`的时候会找不到对应的`label`。一般的形式为：

	\begin{table}
	...
	\caption{This is a table}
	\label{tab:tab1}
	\end{table}

此例中，如果将`\label`放置在`\caption`前面的话会出现上述问题。


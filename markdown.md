Markdown 问题汇总
=====
[回到根目录](./README.md)
##1. 插入图片怎么定义图片的大小或比例
**方法一：**

	![](./pic/pic1_50.png =100x20)
	注意 =前有个空格，可以只写宽度，Mou中支持
**方法二：嵌入HTML代码**

使用img标签

 	<img src="./xxx.png" width = "300" height = "200" alt="图片名称" align=center />

附：如果需要居中的话只要在外面包围div标签即可

	<div  align="center">    
	...
	</div>
参考：[https://www.zhihu.com/question/23378396](https://www.zhihu.com/question/23378396)

##2. Markdown表格中怎么插入逻辑或符号｜？
`%#124;`
也就是Vertical bar的HTML实体。
但不保证所有解释器能正确识别。

参考：[https://www.zhihu.com/question/30409784](https://www.zhihu.com/question/30409784)

##3. Markdown如何换行？
在该行行末输入`<br>`

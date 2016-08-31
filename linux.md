Linux 问题汇总
----
[<< 回到根目录]

### 1.使用wget批量下载文件
参考: <http://tomrose.iteye.com/blog/1055640>

	wget -r http://place.your.url/here

这个命令会按照递归的方法，下载服务器上所有的目录和文件，实质就是下载整个网站。这个命令一定要小心使用，因为在下载的时候，被下载网站指向的所有地址同样会被下载，因此，如果这个网站引用了其他网站，那么被引用的网站也会被下载下来！基于这个原因，这个参数不常用。可以用`-l number`参数来指定下载的层次。例如只下载两层，那么使用`-l 2`。

### 2.访问Windows的共享文件夹
参考: <http://www.howtogeek.com/176471/how-to-share-files-between-windows-and-linux/>

在Windows下建立共享文件夹见[Windows共享某一文件夹(Windows SMB)](./windows.md)。

现在介绍，如何在Linux下访问Windows的共享文件夹。
首先，对于Debian/Ubuntu系统需要安装`cifs-utils`以及`smbclient`，命令如下

	sudo apt-get install cifs-utils
	sudo apt-get install smbclient

然后新建一个文件夹用于挂载windows下的共享文件夹，比如`Windows-Share`,命令如下

	mkdir ~/Desktop/Windows-Share

然后挂载windows下的共享文件夹（假设该文件夹名为`paper`）到刚刚创建的文件夹`~/Desktop/Windows-Share`,命令如下：

	sudo mount.cifs //WindowsPC/Share /place/where/to/put/your/share/fold -o user=your-WindowsPC-name

注意：
- `//WindowsPC/Share`中`WindowsPC`为IP地址，`Share`为WindowsPC共享的文件夹，在此例中为`paper`。
- `/place/where/to/put/your/share/fold`是你在Linux上挂载`paper`的目录，即刚才创建的文件夹`~/Desktop/Windows-Share`，
- `user=your-WindowsPC-name`为你的WindowsPC的用户名，如果你的用户名为`Durant`，那么这里就是`user=Durant`

输完这个代码后，可以在`~/Desktop/Windows-Share`下看到WindowsPC端的共享的`paper`目录中的文件。

## 3. 图形界面下查看隐藏文件
为什么要在图形界面下查看隐藏文件？有一种情况下是十分方便的。由于笔者很久
没有设置环境变量，结果设置`PATH`路径的时候只添加了现在的，之前的所有的
全部失效，要想重新改回来，只有在图形界面显示出隐藏文件才能解决此问题。

在图形界面下，进入`${HOME}`目录，然后按快捷键`CTRL+H`则可显示出该目录下的所有隐藏文件(`.`＋`filename`)。<br>
参考：<br>
[http://www.cnblogs.com/0616--ataozhijia/p/3659688.html](http://www.cnblogs.com/0616--ataozhijia/p/3659688.html)

[<< 回到根目录]: ./README.md

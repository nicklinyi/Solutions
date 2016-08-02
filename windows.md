Windows 相关问题汇总
====
[回到根目录](./README.md)

##1. Windows共享某一文件夹(Windows SMB)
参考：
[1](http://bbs.imp3.net/thread-10488956-1-1.html)
[2](http://jingyan.baidu.com/article/7f766dafbc1af24101e1d012.html)
[3](http://bbs.le.com/thread-358647-1.html)

- 首先找到要共享的文件夹，然后`右键`该文件夹，弹出一个新窗口，为`XX属性`；
- 选择导航条的第二个`共享`，可以发现有两个按钮：`共享(S)...`和`高级共享(D)...`；
- 选择第一个按钮`共享(S)...`，弹出一个新的对话框，然后在`添加(A)`左侧有个下拉选项；
- 选择下拉选项中的`Everyone`,然后点击`添加(A)`,接着点击下面的`共享(H)`,文件夹部分设置
完毕;
- 最后一步，打开`网络和共享中心`-->`更改高级共享设置`-->`密码保护的共享`-->`关闭密码保
护共享`-->`保持修改`即可。

##2. 在所有的文件右键菜单中加入自定义的命令
参考：
[http://www.phpvar.com/archives/251.html](http://www.phpvar.com/archives/251.html)

- 打开`HKEY_CLASSES_ROOT\*`；
- 在其下新建`shell\(自定义的提示符(如：Open With Sublime Text))\command`分支，再将
`command`的键值设为执行该命令时所用的可执行程序的绝对路径，并在其后加`%1`即可。

##3. 怎么打出箭头符号（非LaTeX环境）
在输入法的小面板上右键→软键盘→特殊符号→选择需要的箭头	
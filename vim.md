VIM
------
[回到根目录](./README.md)

###Vim中显示不可见字符
参考资料：[http://yejinxin.github.io/show-nonprinting-character-in-vim/](http://yejinxin.github.io/show-nonprinting-character-in-vim/)
只需要`:set invlist`即可以将不可见的字符显示出来，例如，会以`^I`表示一个`tab`符，`$`表示一个回车符等。

或者，你还可以自己定义不可见字符的显示方式：

    set listchars=eol:$,tab:>-,trail:~,extends:>,precedes:<
    set list

最后，`:set nolist`可以回到正常的模式。

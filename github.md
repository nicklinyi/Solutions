Git 问题汇总
----
[<< 回到根目录]

### 1.github Contributions Calendar 没有显示自己的 commit 记录。
参考: <https://www.zhihu.com/question/21371544>
一般是git config出错了。
重新设置你github 的账号和邮箱即可

	git config --global user.name [username]
	git config --global user.email [email]

### 2.添加多个SSH key之后验证失败 
参考: <http://blog.csdn.net/carolzhang8406/article/details/23746317>

解决方案:

	ssh-add ~/.ssh/id_rsa

注意这儿是`id_rsa`,而不是`id_rsa.pub`

[<< 回到根目录]: ./README.md

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

### 3.查看分支情况
参考:<https://git-scm.com/book/zh/v1/Git-%E5%88%86%E6%94%AF-%E5%88%86%E6%94%AF%E7%9A%84%E7%AE%A1%E7%90%86>
`git branch`命令不仅仅能创建和删除分支，如果不加任何参数，它会给出当前所有分支的清单：

	$ git branch
  	  iss53
	* master
  	  testing

注意看 `master` 分支前的 `*` 字符：它表示当前所在的分支。也就是说，如果现在提交更新，`master` 分支将随着开发进度前移。若要查看各个分支最后一个提交对象的信息，运行 `git branch -v`：

	$ git branch -v
      iss53   93b412c fix javascript issue
	* master  7a98805 Merge branch 'iss53'
      testing 782fd34 add scott to the author list in the readmes

### 4.`git push -u origin master`出错
参考：<http://stackoverflow.com/questions/15637507/fatal-origin-does-not-appear-to-be-a-git-repository>

出错情况为

	$ git push -u orgin master
	fatal: 'orgin' does not appear to be a git repository
	fatal: Could not read from remote repository.

	Please make sure you have the correct access rights
	and the repository exists.

解决方案：
首先，查看`git remote -v`是否显示`orgin`,正确的结果如下

	$ git remote -v
	origin  git@github.com:nick/Solutions.git (fetch)
	origin  git@github.com:nick/Solutions.git (push)

如果正确的话，修改命令`git push -u origin master`为`git push  origin master`，即可成功上传至`repo`。


[<< 回到根目录]: ./README.md

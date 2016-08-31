Linux 问题汇总
----
[<< 回到根目录]

### 1. Problem with Bash script:'declare: not found'
出现这种情况的原因在于在脚本的第一行采用`sh`而非`bash`。因为`sh`与`dash`联接，它不支持`declare`,以及`VAR=(list)`(初始化数列)这样的语法。

应在脚本的第一行书写`#!/bin/bash`。<br>
参考:<br>
[http://askubuntu.com/questions/28311/problem-with-bash-script-declare-not-found](http://askubuntu.com/questions/28311/problem-with-bash-script-declare-not-found)




[<< 回到根目录]: ./README.md

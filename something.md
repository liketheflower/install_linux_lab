# source not found
ubuntu 默认shell为dash进行解析 。而redhat 默认为bash。dash比dash要弱。

解决方案：

sh文件中头部

 #! /bin/sh
Change that to the following (you can preserve any options you see):

 #! /bin/bash
在 Makefiles, you can set the following variable at the top:

SHELL = /bin/bash
如果问题比较普遍把dash替换为bash
If the problems are more widespread and you want to change the default system shell back, then you can instruct the package management system to stop installing dash as /bin/sh:

sudo dpkg-reconfigure dash
在弹出界面选NO

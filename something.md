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


Wierd, I run 
sudo dpkg-reconfigure dash
在弹出界面选YES

It worked...

#  Arrow keys, tab-complete not working

sudo chsh -s /bin/bash <username>
 
 
 https://askubuntu.com/questions/325807/arrow-keys-tab-complete-not-working
 
 
 
 # change the default gcc version
 Thanks to you all for your help. I ended up just creating aliases within ~/.bash_profile as follows:

alias gcc='gcc-4.8'
alias cc='gcc-4.8'
alias g++='g++-4.8'
alias c++='c++-4.8'


#  reinstall gcc
https://gist.github.com/application2000/73fd6f4bf1be6600a2cf9f56315a2d91

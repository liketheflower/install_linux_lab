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






# source activate is not working properly

# clear the content of the file by typing
```sh
echo $PATH
export PATH="ONLY CONTAIN THE BASIC PATH AND REMOVE THE ANACONDA PATH"
vi ~/.bashrc

```

content of the "~/.bashrc"
```
export PATH="/usr/local/bin:$PATH"
export PATH=/usr/local/cuda-8.0/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-8.0/lib${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
export PATH="~/anaconda/bin:$PATH"
```


```
source ~/.bashrc
conda env list
conda deactivate
conda activate
```


# delete the local unpushed commits

Delete the most recent commit:

git reset --hard HEAD~1
Delete the most recent commit, without destroying the work you've done:

git reset --soft HEAD~1

# Asking username and password for many times
Are you saying credential caching isn't working for you? What does git config -l | grep credential return? I think it is off by default.

You can turn it on (on Linux) like so:

git config --global credential.helper cache

# git Large file mangement
https://github.com/git-lfs/git-lfs/wiki/Installation

https://github.com/git-lfs/git-lfs

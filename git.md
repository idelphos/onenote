#git

###install Git on RHEL
1. `yum install git`
2.  install from source code

``` 
refer to [README.md](https://github.com/git/git/blob/master/README.md)
[download git source code](https://github.com/git/git/releases/)
tar -zxvf git-1.7.9.4.tat.gz
$make configure
$./configure --prefix=/usr　--with-curl --with-expat　配置安装程序目录
$make all doc
\#make install install-doc install-html;# as root
git --version   verfiy the installation
```

###配置Ｇit
git config --global user.name "Ade"
git config --global user.email "adelphos@msn.cn"
cat ~/.gitconfig


###配置[github](https://github.com）
setting 里添加本地ssh public key
`ssh -T git@github.com` 进行测试

####免密码push
git remote -v       查看使用的传输协议，不要使用https

设置成ssh方式
git remote rm origin
git remote add origin git@github.com:username/repository.git
git push -u origin master



###known git issue

fatal: Unable to find remote helper for 'https'
无权限执行git-remote-https

PATH=$PATH:/usr/libexec/git-core./configure --prefix=/usr --with-curl --with-expat


yum install libcurl-devel 
重新编译安装

----

```
1）git clone已存在GitHub上的Repository。（在新建的~/MyTestFolder目录中）

git clone https://github.com/zhchnchn/ZhchnchnTest.git

（2）修改一个文件，然后提交

vim README.md
git status
git add README.md
git status
git commit -m "Edit by WorkUbuntu 1204"
git status
git remote add origin https://github.com/zhchnchn/ZhchnchnTest.git

这时会报错误：

fatal: remote origin already exists.

解决办法【3】：

$ git remote rm origin

然后再次执行 git remote add origin https://github.com/zhchnchn/ZhchnchnTest.git

（3）之后，需要将修改push到GitHub上

git push -u origin master

执行该条命令后，会要求输入GitHub账户的用户名和密码。

（4）提交完成后，查看GitHub上的Repository，会发现内容修改成功。

```



###Git 快速入门






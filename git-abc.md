

###git 快速手册
git init         

git log 
git status
git commit -m "comments"
git add b.txt
git commit -a 


git clone https://github.com/idelphos/onenote.git     克隆仓库至本地

git push



###远程提交代码
新建仓库
[github](https://github.com/idelphos/onenote.git)

git init          初始化本地文件夹,目录下建仓库.git
git add .         提交更改，先提交代码至缓存区,
git commit -m "comment"   　　实际提交代码

git remote add origin <server>   　　连接到远程仓库
git push origin master 　　　　　　　　提交变更到远程仓库

`git add <files>`
git add 可多次提交，然后使用git commit 一次提交至仓库



git status        查询仓库状态
git diff          查看修改的内容
git log　         命令显示从最近到最远的提交日志















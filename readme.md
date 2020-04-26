cd 路径		//进入当前目录
配置git基本操作，没有消息就是好消息
git init		//在本地进行初始化，建立暂存区，会生成一个.git文件
工作区=>暂存区
git add 文件名
git remote add origin 地址		这是首先第一步
git add * 提交所有文件	①
git commit -m“对这次提交的描述”		②
git status		//查看当前工作区的状态		③
git diff		//查看工作区和暂存区的区别
clear			//清屏操作
git log		//查看历史提交版本
git reset --hard 版本号	//即可恢复历史需要的版本
git reset --hard HEAD^退回到上一版本
git reset --hard HEAD^^退回到上两个版本
账户配置GitHub密钥
ssh-keygen -t rsa -C ”github邮箱号”
cd ~/.ssh   （如果没有执行第三步，则不会有这个文件夹）
cat id_rsa.pub     在命令行打开这个文件，会直接输出密钥
打开github   ，点自己头像 >> settings >> SSH and GPG keys >>New SSH key
暂存区=>远程仓库
git remote add origin 地址		④
git push -u origin master			⑤
若有修改，第二次提交
①②③直接git push 就ok了，前面的提交步骤不用做了
git clone	地址	//从远程仓库，克隆项目到本地。记得选好目录路径
git pull			//克隆到了本地以后，原版远程仓库代码有可能会被修改更新，这个是同步更新的意思

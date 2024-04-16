git

# git
## 新建仓库
### git init and git clone
找到一个合适的位置找到一个目录
```bash
mkdir learn-git;//创建一个空目录
cd learn-fit;//change directory
//wqb@LAPTOP-VQ01AAAC MINGW64 ~/learn-git (master)表示当前目录已经是一个被git 管理的仓库
ls -a;//显示隐藏文件，说明git 仓库被建立成功
git init my-repo //创建仓库
```

## 工作区 暂存区 本地仓库
working directory  staging area/index  local repository  
首先将工作区的内容提交到暂存区

### git文件状态
未跟踪：untrack  没有被git管理
未修改：已经被git管理，但是没有被修改
已修改：
已暂存：

## 主要指令
```bash
cd    用来改变目录，change directory
git config    初始化姓名和邮箱，只需要配置一次
git status    查看仓库状态
git add     添加到暂存区
git commit -m    添加到仓库，不加-m的话会调出vim
git log    查看仓库日志，更新的时间地点
git log --oneline 提交信息简洁版
echo "" >     往一个文件中传入信息
git add . 添加全部文件
git add *.txt 添加txt后缀的文件
cd 创造文件
ls  list directory contents
cat file1.txt 读取文件中的内容
git branch 查看所在分支
git branch -r 查看远程分支
git checkout master 切换master分支
git remote -v 查看当前仓库的别名和地址
git pull 远程仓库名 远程分支 本地分支   拉取远程仓库，执行完pull后，会自动进行合并操作
git fetch 只是拉取修改不会合并，，需要手动合并
```

### git常用指令

安装后设置用户名

```txt
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

```js
//常用指令
git init 	初始化，使文件夹变成仓库管理
git add 文件名 	把文件添加到仓库// ./选择所有文件
git commit -m "说明" 	将文件提交到仓库
git commit --all -m "说明"   将所有代码一次性操作

git status 	 查看仓库与当前版本的区别
```

##### 忽略文件

```js
.gitignore 文件

/.idea
/.gitignore
```

##### 版本回退

```txt
git log 查看所有版本 --pretty=oneline参数(简写)
git log --oneline // 记录当前拥有的

git reset --hard HEAD^ 回退至上一个版本
git reset --hard HEAD^^回退两个版本
git reset --hard HEAD 0~100回退100个版本

git reflog //记录所有的

git reset --hard d38870e 指定版本


```

##### 修改

```js
git diff HEAD -- readme.txt 查看修改内容
git checkout -- file 丢弃工作区的修改
git reset HEAD <file> 将暂存区的修改撤销掉

```

##### 删除

```txt
git rm test.txt 删除
```

##### 创建与合并分支

```txt
git checkout -b dev 创建一个分支

$ git branch dev//创建分支
$ git checkout dev // 切换至dev分支

然后修改内容
之后添加 提交
$ git add readme.txt 
$ git commit -m "branch test"

切换到master分支
git checkout master
发现修改的内容没有了

之后合并分支
git merge dev

然后删除分支
$ git branch -d dev 

git branch 查看所有分支 *表示当前分支
发现只剩下一个分支了

git switch -c dev 最新版本的切换分支

git switch master 切换到master分支
```

##### 解决冲突

```txt
git switch -c feature1
创建一个分支

修改内容 提交

切换到master版本 修改 提交

git merge feature1 合并的时候冲突

手动修改之后就可以了

再提交之后 删除就可以了

```

##### 远程仓库

```txt
github

https://github.com/18437826577/git.git


git push  -u  origin master 将本地分支master推送过去

git add 

git commit -m

git push [地址] master  提交

// 获取
git pill [地址] master

//
git clone [地址]

```












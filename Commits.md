# Commits 提交

### 查看已提交内容
`(main)$ git show`  
或者
`$ git log -n1 -p`

如果想要查看一个文件在某次特殊的提交中的修改记录：
`$ git show <commitid>:filename`

### 提交信息写错了
如果你的提交还没推上去，则可以修改：  
`$ git commit --amend --only -m 'xxxxxxx'`

### 用了错误的名字和邮箱去提交
`$ git commit --amend --no-edit --author "New Authorname <authoremail@mydomain.com>"`

### 想要从之前的提交中移除某些文件
```
$ git checkout HEAD^ myfile
$ git add myfile
$ git commit --amend --no-edit
```
这样myfile就是新被添加的文件，然后要删除它：  
```
$ git rm --cached myfile
$ git commit --amend --no-edit
```

### 想要贡献代码到别人的项目
首先fork项目到自己的账号并复制url，然后运行：  
`$ git clone [fork url]`  
然后进入项目修改完毕后，运行：   
`$ git remote add upstream [origin url]`  
就可以进行push操作了


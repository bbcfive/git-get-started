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

### 想要删除最后一次提交
如果已经推上去了，不建议删除。  
如果还没推，则可以重置git状态到提交前，同时能够保留所做修改：
`(my-branch*)$ git reset --soft HEAD@{1}`  



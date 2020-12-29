# Stash 隐匿

### 隐匿所有当前工作目录下的编辑，包括未跟踪文件
`$ git stash -u`

### 隐匿文件并上传信息
```
$ git stash save <message>
or 
$ git stash push -m <message>
```

### 应用隐匿文件
查找所有列表：  
`$ git stash list`  
根据携带信息应用相应文件：  
`$ git stash apply "stash@{n}"`

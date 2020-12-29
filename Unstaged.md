# Unstaged Edits 未存编辑

### 把未保存编辑移到新分支
`$ git checkout -b my-branch`

### 把未保存的编辑移到已存在的分支
```
$ git stash
$ git checkout my-branch
$ git stash pop
```

### 废弃本地的未提交文件(包括已存和未存文件)
还原所有文件成未存文件：
```
(my-branch)$ git reset --hard
# or
(main)$ git checkout -f
```
删除未存文件：
`$ git clean -fd`

### 废弃本地所有暂存区文件
`$ git checkout .`

### 废弃本地所有未存的文件
`$ git clean -f`

### 废弃本地某个暂存区文件
`$ git reset -- <filename>`


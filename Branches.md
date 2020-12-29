# Branches 分支

### 显示本地所有分支
`$ git branch`  

### 显示远程所有分支
`$ git branch -r`  

### 显示所有分支(本地/远程)
`$ git branch -a`  

### 从已提交的文件创建分支
`$ git checkout -b <branch>`  

### 拉错了分支
先查看当前的HEAD指向：
```
(main)$ git reflog
ab7555f HEAD@{0}: pull origin wrong-branch: Fast-forward
c5bc55a HEAD@{1}: checkout: checkout message goes here
```  
再把分支重设为想要的提交： 
`$ git reset --hard c5bc55a` 

### 废弃本地的提交
显示本地已提交内容：  
`(my-branch)$ git status`  
回退到源分支：  
`(main)$ git reset --hard origin/my-branch`

### 回退到上一版本
`(main)$ git reset --hard HEAD^1`  

### 删除所有本地已合并的分支
`$ git fetch -p upstream`  

### 删除本地所有分支
`$ git branch | grep -v "master" | xargs git branch -D `

### 删除本地所有以'fix/'开头的分支
`(main)$ git branch | grep 'fix/' | xargs git branch -D`

### 重新命名分支
`(main)$ git branch -m new-name` 

### 为本地分支设置远程分支作为上游
```
$ git branch --set-upstream-to [remotename]/[branch]
# or, using the shorthand:
$ git branch -u [remotename]/[branch]
``` 

### 在错误的分支上做了改变
```
(wrong_branch)$ git stash
(wrong_branch)$ git checkout <correct_branch>
(correct_branch)$ git stash apply
``` 
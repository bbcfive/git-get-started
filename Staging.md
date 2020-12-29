# Staging 暂存区操作

### 暂存所有已跟踪的文件并且放弃所有未跟踪的文件
`$ git add -u`

### 把暂存区的改变加入之前的提交中
`(my-branch*)$ git commit --amend`

### 把部分文件而非全部文件加入暂存区
`$ git add --patch filename.x`

### 如果filename.x是个新文件
`$ git add -N filename.x`

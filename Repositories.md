# Repository 仓库

### 将本地已存在的目录初始化成一个Git仓库
`(my-folder) $ git init`

### 将目录下的所有文件上传到暂存区，也可以将“.”换成具体的文件名
`git add .`

### 将项目提交到本地仓库
`git commit -m "xxx"`

### 将本地的代码关联到github上
`git remote add origin [url]`

### 将本地提交推到github上
`git push -u origin master`

### 想要克隆一个远程仓库
先复制仓库URl，然后运行：  
`$ git clone [url]`

### 想要克隆它并重新为其命名而非用默认的仓库名
`$ git clone [url] name-of-new-folder`


### 设置错远程仓库
需要更改源地址：  
`$ git remote set-url origin [url of the actual repo]`

### 想要贡献代码到别人的项目
首先fork项目到自己的账号并复制url，然后运行：  
`$ git clone [fork url]`  
然后进入项目修改完毕后，运行：   
`$ git remote add upstream [origin url]`  
就可以进行push操作了



# Finding 查找

### 查找包含此字符串的所有提交
`$ git log -S "string to find"`

### 查找某一作者/贡献者的提交
```
$ git log --author=<name or email>
$ git log --committer=<name or email>
```

### 查找包含此文件的所有提交
`$ git log -- <path to file>`

### 查找某特定函数的提交历史
`$ git log -L :FunctionName:FilePath`

### 查找某次提交所包含的所有标签
`$ git tag --contains <commitid>`

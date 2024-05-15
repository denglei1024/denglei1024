我从github上下载了mybatis-parent项目，然后使用maven构建时报了这个错误。

不在.git目录下构建就会报错。

解决办法
1、初始化git仓库
```
git init
```
2、添加远程地址
```
git remote add origin <远程仓库地址>
```

或者重新使用git clone下载
```
git clone <远程仓库地址>
```
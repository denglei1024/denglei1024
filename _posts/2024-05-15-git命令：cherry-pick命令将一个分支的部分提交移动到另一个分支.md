
git cherry-pick可以将一个分支上的commit应用到其他分支，演示示例

要把Feature分支的f、g提交应用到Master
```
a-b-c-d-e Master
	  \
	   e-f-g Feature
```
1、切换到Master
``` 
git checkout master
```

2、挑拣
```
git cherry-pick f g
# f、g 是这两个提交的commit hash
```

应用后，f、g会以commit的方式应用到Master，hash会变
```
a-b-c-d-e-f-g Master
	  \
	   e-f-g Feature
```

## <font style="color:#2F4BDA;">Level4</font>
### <font style="color:#2F4BDA;">谜题</font>
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

![](images/level4.png)

### <font style="color:#2F4BDA;">解题思路</font>
问题：目录下有多个文件，需要找到可读文件的内容

方法：多文件读取

### <font style="color:#2F4BDA;">最终命令</font>
```shell
cat ./*
```
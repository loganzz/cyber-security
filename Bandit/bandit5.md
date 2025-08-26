## <font style="color:#2F4BDA;">Level5</font>
### <font style="color:#2F4BDA;">谜题</font>
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

1、human-readable
2、1033 bytes in size
3、not executable
![](images/level5.png)

### <font style="color:#2F4BDA;">解题思路</font>
问题：目录下有多个子目录，需要找到子目录下的可读、不可执行、大小为<font style="color:rgb(0, 0, 0);">1033字节的文件</font>

方法：find 筛选查找

### <font style="color:#2F4BDA;">最终命令</font>
```shell
find . -type f -size 1033c -not -executable -exec cat {} +
```

下面是对该命令的解释：

+ `find .`：在当前目录（`.`）及其子目录中查找。
+ `-type f`：只查找文件（`f`）。
+ `-size 1033c`：查找大小为1033字节（`c`）的文件。
+ `-not -executable`：查找不可执行的文件。
+ `{}`: 这是一个占位符，代表 `find` 命令找到的每一个文件。当 `find` 找到一个文件时，它会把这个文件的路径名替换到 `{}` 的位置。
+ `+`: 这是一个特殊的结束符，表示 `find` 命令应该将所有找到的文件一次性作为参数传递给 `exec` 命令，而不是为每个文件都执行一次(如`;` 结束符)。这大大提高了效率，尤其是在文件数量很多的情况下。
+ `-exec cat {} +`：找到所有文件后，会执行 `cat` 命令。
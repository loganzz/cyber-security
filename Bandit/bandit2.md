## <font style="color:#2F4BDA;">Level2</font>
### <font style="color:#2F4BDA;">谜题</font>
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory
### <font style="color:#2F4BDA;">解题思路</font>
问题：文件名为"<font style="color:rgb(0, 0, 0);">--spaces in this filename--</font>"，直接用`cat --spaces in this filename--` shell会理解出错，将--space解释为一个选项

方法：需要将space进行转义

### <font style="color:#2F4BDA;">最终命令</font>
```shell
cat ./--spaces\ in\ this\ filename--
```
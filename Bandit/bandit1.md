## <font style="color:#2F4BDA;">Level1</font>
### <font style="color:#2F4BDA;">谜题</font>
The password for the next level is stored in a file called - located in the home directory
### <font style="color:#2F4BDA;">解题思路</font>
问题：文件名为"-"，直接用`cat -` shell会理解出错，将前导破折号解释为一个选项

方法：有三种方法可以进行规避  
1、使用./前缀

2、使用--作为选项结束标记，表示不应将任何进一步的参数解释为选项

3、用单引号或双引号括起文件名可以防止shell将前导破折号解释为一个选项

### <font style="color:#2F4BDA;">最终命令</font>
```shell
cat ./-
```
## <font style="color:#2F4BDA;">Level7</font>
### <font style="color:#2F4BDA;">谜题</font>
The password for the next level is stored in the file data.txt next to the word millionth

### <font style="color:#2F4BDA;">解题思路</font>
问题：需要找到data.txt文件中紧跟着`millionth`的密码

方法：管道 + grep 筛选查找

### <font style="color:#2F4BDA;">最终命令</font>
```shell
cat data.txt | grep millionth
```

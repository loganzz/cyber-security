## <font style="color:#2F4BDA;">Level6</font>
### <font style="color:#2F4BDA;">谜题</font>
The password for the next level is stored somewhere on the server and has all of the following properties:

1、owned by user bandit7
2、owned by group bandit6
3、33 bytes in size
### <font style="color:#2F4BDA;">解题思路</font>
问题：需要找到当前服务器下的所有者为 `bandit7`、所属组为 `bandit6`、大小为<font style="color:rgb(0, 0, 0);">33字节的文件</font>

方法：find 筛选查找

### <font style="color:#2F4BDA;">最终命令</font>
```shell
find / -type f -user bandit7 -group bandit6 -size 33c
cat /var/lib/dpkg/info/bandit7.password
```
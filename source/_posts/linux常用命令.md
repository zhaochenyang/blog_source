---
title: Linux 常用命令
tags:
    - shell
    - linux
---

总结一下常用的linux命令，以备不时之需。
## Userful Command

### tar

创建新的压缩文件
> $ tar cvf archive_name.tar dirname/

解压现有文件
> $ tar xvf archive_name.tar

更多实例信息 [The Ultimate Tar Command Tutorial with 10 Practical Examples](https://www.thegeekstuff.com/2010/04/unix-tar-command-examples/)

### grep

匹配查询一个词语,大小写不敏感用-i
> $ grep -i "the" demo_file

查询返回匹配行及后面3行
> $ grep -A 3 -i "example" demo_text

递归查询文件夹文件
> $ grep -r "ramesh" *

正则表达式
> $ grep "lines.*empty" demo_file
> Two lines above this line is empty.

不展示所有pattern
> $ cat test-file.txt
a
b
c
d
> $ grep -v -e "a" -e "b" -e "c" test-file.txt
d

Count lines matched
> $ grep -c "go" demo_text
6
$ grep "go" demo_text |wc -l

更多实例: [Get a Grip on the Grep! – 15 Practical Grep Command Examples](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)

### find

查找文件名 -i 大小写不敏感
> $ find -iname "MyCProgram.c"

### Referrence

* https://www.thegeekstuff.com/2010/11/50-linux-commands/?utm_source=feedburner

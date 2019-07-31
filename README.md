# Git-commend

Local> Global >System

**git init**
初始化github repository

**edit file**

    vi + filename //edit file
    i //insert
    :wq //save and exit
    
**git status**
查看状态

**git add+filename**
把文件存放在暂存器

**git commit -m + description**
commit文件

### **Diff**

**git diff**
找出项目中哪些地方被改动了，通过这个命令，对你的工作树的精确描述，也就是，仅仅是你的文件，而不同于你的暂存区域。

**git diff --staged**
暂存区域文件和最近提交的历史文件的区别

**git diff HEAD**
将你的工作树和头一次提交相比较，这只是在提交历史中最近一次提交的另一个别名。

**git diff --color-words**
**git diff --word-diff**
一种对长行小改动而言更易读的报告
**git diff --stat**
让Diff阻止输出所有的代码块，而是仅仅输出更改了的文件。

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

### **Log**

**git log**查看编辑日志
**git log --oneline** 更简略
**git log --stat** 更详细，包括了提交包含的文件以及内容的增加或减少
**git log --patch** 包含了修改的细节

### **Remove**
**git rm +filename**
如果你只有一个文件想要删除，使用这个命令可以真正的从文件系统中删除了文件，并且它会暂存这个文件已经被删除的事实，如果你提交了，这个文件不会从之前的历史中消失，但会从未来的提交中消失。
**git add -u .**
会遍历你的工作树，寻找Git之前已经识别到的文件，现在要消失的文件，它会把他们作为新的删除来暂存，这里输入了一个点作为文件名字，那只是意味着当前工作目录的简写，当它看到add时，它会从你当前所在的目录递归到最深处寻找它能够添加的所有文件，或者说，在这个场景下，所有能够被删除的文件。
**需要注意的是，2.0版本后的git add已经和git add -A效果相同，因此只需要记住git add .这个命令就可以了**

**git rm --cached +filename**
使github不再追踪这个文件，但是保留在你的工作树中

### **Move**
**git mv +oldPath +newPath**
git已经暂存了move发生的事实，但是，如果你只是简单的使用mv命令来移动文件，然后忘了告诉git，Git注意到，某个地方出现了一个本不应该出现的新文件，它同时注意到原来的文件区域已经被删除掉了，我们可以一次一个步骤来解决它：
**git rm**
删除原来的文件
**git add production.log**
添加新文件
当我们做这些的时候，状态把这些拼在一起了，告诉我们一个移动已经发生了。

### git ignore

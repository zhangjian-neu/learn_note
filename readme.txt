This is just an example.
It should be in  ~/learngit


Git is a version control system.
Git is free software.


小结1
初始化一个Git仓库，使用git init命令。

添加文件到Git仓库，分两步：

    第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；

    第二步，使用命令git commit，完成

版本回退 小结
    HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。

    穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。

    要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。
    
工作区与暂存区 小结
    工作区就是你在电脑里能看到的目录，比如我的learngit文件夹就是一个工作区。
    工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。
    Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。
    
网友理解 git diff
    git diff    #是工作区(work dict)和暂存区(stage)的比较
    git diff --cached    #是暂存区(stage)和分支(master)的比较
    
管理修改 小结
    为什么Git比其他版本控制系统设计得优秀，因为Git跟踪并管理的是修改，而非文件。
    cat <filename> 其功能是显示在工作区、暂存区和分支里同名文档的最新修改版本的内容。

撤销修改 小结
    1. 命令git checkout readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：

    一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

    一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

    总之，就是让这个文件回到最近一次git commit或git add时的状态。
    
    2. 在commit之前, 命令git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区.
    3.假设你不但改错了东西，还从暂存区提交到了版本库，怎么办呢？还记得版本回退一节吗？可以回退到上一个版本。不过，这是有条件的，就是你还没有把自己的本地版本库推送到远程。还记得Git是分布式版本控制系统吗？我们后面会讲到远程版本库，一旦你把“stupid boss”提交推送到远程版本库，你就真的惨了……

删除修改 小结
    
    一般情况下，你通常直接在文件管理器中把没用的文件删了，或者用rm命令删了：
    $ rm test.txt
    
    这个时候，Git知道你删除了文件，因此，工作区和版本库就不一致了，git status命令会立刻告诉你哪些文件被删除了。
    
    现在你有两个选择，一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit。
    
    另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
    $ git checkout -- test.txt
    git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还。
    
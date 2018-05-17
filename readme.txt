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
    工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。
    Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。
    
网友理解 git diff
    git diff    #是工作区(work dict)和暂存区(stage)的比较
    git diff --cached    #是暂存区(stage)和分支(master)的比较
    
管理修改 小结
    为什么Git比其他版本控制系统设计得优秀，因为Git跟踪并管理的是修改，而非文件。
    
change 1
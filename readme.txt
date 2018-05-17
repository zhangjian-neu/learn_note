This is just an example.
It should be in  ~/learngit

廖雪峰网站
https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000


创建文本库 小结
    创建一个版本库非常简单，首先，选择一个合适的地方，创建一个空目录：

    $ mkdir learngit
    $ cd learngit
    $ pwd
    /Users/michael/learngit
    pwd命令用于显示当前目录。在我的Mac上，这个仓库位于/Users/michael/learngit。

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
    1. 文件已修改，未add到暂存区:
    git checkout -- file可还原

    2. 文件已修改，并add到暂存区未commit：
    git read HEAD file
    git checkout -- file可还原
    3.假设你不但改错了东西，还从暂存区提交到了版本库，怎么办呢？还记得版本回退一节吗？可以回退到上一个版本。不过，这是有条件的，就是你还没有把自己的本地版本库推送到远程。还记得Git是分布式版本控制系统吗？我们后面会讲到远程版本库，一旦你把“stupid boss”提交推送到远程版本库，你就真的惨了……

删除修改 小结
    
    一般情况下，你通常直接在文件管理器中把没用的文件删了，或者用rm命令删了：
    $ rm test.txt
    
    这个时候，Git知道你删除了文件，因此，工作区和版本库就不一致了，git status命令会立刻告诉你哪些文件被删除了。
    
    现在你有两个选择，一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit。
    
    另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
    $ git checkout -- test.txt
    git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还。
    
设置 SSH
    1. 在主目录下，使用 $ ssh-keygen -t rsa -C "youremail@example.com" 创建ssh key。
    在github网站的步骤为：登录网站--点击我的头像，找到Settings--屏幕左侧找到SSH and GPG keys
    
    2. 使用 ssh -T git@github.com 测试当前电脑是否github网站成功连接。如果未成功，删除.ssh文件夹，从新生成ssh key， 然后在网站上从新设置。
    
    3. 使用命令 $ cd ~/learngit， 然后使用$ git remote add origin git@github.com:michaelliao/learngit.git 或者 $ git push -u origin master 推送
    把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。

clone
    使用命令$ git clone git@github.com...
    如果有多个人协作开发，那么每个人各自从远程克隆一份就可以了。
    
分支
    大家在使用同一个版本库时，每个人可以创建一个分支，用于保存自己目前尚未完成的工作。
    首先，我们创建dev分支，然后切换到dev分支：

创建分支    
    查看分支：git branch

    创建分支：git branch <name>

    切换分支：git checkout <name>

    创建+切换分支：git checkout -b <name>

    合并某分支到当前分支：git merge <name>

    删除分支：git branch -d <name>
    
解决冲突
    当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。
    用git log --graph命令可以看到分支合并图。

    

bug
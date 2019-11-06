this is the file for learn git
git --version                               #查看版本号
git config --global user.name "姓名"        #git 使用前配置
git config --global user.email "email"
git config --global core.editor "code -w"
git config --list                            #查看配置
或在使用者目录下 code .gitconfig
q 退出
以下在工作目录下执行 pwd                      #打印工作目录
git init                    #当前目录下的 .git 子目录下初始化了一个空的 repo
ls -la 或 ls -Force         #显示该文件
git status                  #显示目前工作目录的状态
touch README.md             #创建一个空的名为 README.md 的文件
code README.md              #用 VSCode 打开这个空的文件
git add README.md           #有变化的文件加入待提交的“暂存区域（staging area）”对 untracked files 它具有双重功效，先将其加入到版本管理中（从 untracked 变成 tracked），再加入 staging area
git commit                   #在 staging area 的任何文件变化到版本仓库
git checkout --README.md    #git checkout 从版本仓库中取得一个文件的指定版本，然后覆盖到工作目录中。命令后面可以指定一个 commit id，上面我们用 -- 就表示从仓库里最新的一个 commit 中取，最后是要取出的文件路径（当前目录下 README.md 文件）。运行上面的命令会废弃掉（discard）刚才对 README.md 做的修改
git add .           # 将当前目录及其下面变化的所有文件都加入到 staging area 
git reset HEAD README.md  #从 staging area 移出来
git restore --staged README.md  #同上变为unstaging
git log                         #看版本的历史记录,从新到旧排列
git checkout 7451a00            #回到了你最初提交 README.md 一个文件的状态
git checkout master             #回到了最新的状态
git diff 7451a00                #比较指定 commit 和工作目录当前状态
git diff 7451a00 5d4f3df README.md        #比较两个指定的 commit
git clone https://github.com/keleyuan/learn-git.git #clone git内容
git  commit -a -m "++clone"      #直接变为版本仓库
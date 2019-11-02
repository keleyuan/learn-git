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
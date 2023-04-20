# git-demo

[toc]

learning git

## Clone and Commit

- git clone: clone repository to the local machine
- git status: check the modified files and untracked files
- git add
  - git add. Add all of the files  to GitHub
- git commit -m “Update XX” -m “some description”
  第一个m代表此次修改描述的题目，第二个m代表此次修改的具体描述
  - git commit -a -m "some title" # 快捷方式，同时实现add, commit, 但仅适用于非第一次创建的文件

## 构建ssh key

1. 首先在本地终端中输入

```bash
ssh-keygen -t rsa -b 4096 -C "shuyuan.w@pku.edu.cn" # 4096代表文件长度
eval “$(ssh-agent -s)” # mac用户需要对config做修改
```

2. 在github中的sshkey中输入rsa.pub中的内容

## Push and Pull

- git push: push the local files to a remote repository where my project is host
  - git push -u origin master/main (-u代表后面是default内容，以后就不用再输入), origin: local of our git repository; master: remote
- git pull # local 从remote中拉取
  - git pull origin main

## Branch

- git branch: 查看分支
- git checkout: switch between branches
  - git checkout -b branch_name: create a new branch
- git diff: shows what changes have been made, it compares two versions
  - git diff sy-test-branch (branch name)
- git merge main: 将branch中的内容整合到main
  - 如果产生冲突，可以直接在冲突文件中使用Vscode进行修改
- git push -u origin sy-test-branch #将分支内容push到remote,同时提交pull request

## Undo

## Local Development

- git log # 查看全部commits记录,注意commit id
- git reset # 撤回上一次add操作
  - git reset HEAD~1 # HEAD指commit, 1是上一次，撤回上一次commit操作
  - git reset commit_id #  该commit的操作 unstaged
  - git reset --hard commit_id # remove 该commit的操作
- git show-ref:确认是main or master
- git rebase -i (commit_id): 回到commit, 修改commit状态

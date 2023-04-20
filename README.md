# git-demo

learning git

- git clone: clone repository to the local machine
- git status: check the modified files and untracked files

- git add
  - git add. Add all of the files  to GitHub

- git commit -m “Update XX” -m “some description”
  第一个m代表此次修改描述的题目，第二个m代表此次修改的具体描述

- 构建ssh key

```bash
ssh-keygen -t rsa -b 4096 -C "shuyuan.w@pku.edu.cn"
eval “$(ssh-agent -s)” # mac用户
```

- git push: push the local files to a remote repository where my project is host
  - git push -u origin master/main (-u代表后面是default内容，以后就不用再输入), origin: local of our git repository; master: remote
- git show-ref:确认是main or master
- git log: 查看commit记录
- git rebase -i (commit_id) : 回到commit, 修改commit状态
- git branch: 查看分支
- git checkout: switch between branches
  - git checkout -b branch_name: create a new branch


## TBD

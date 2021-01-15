# Commands

### Git

```bash
# reset file to unmodified state
  git checkout [file]

# switch to branch
  git checkout -b [branch_name]

# ------

# pick up other commits to merge
  git cherry-pick [commit_1] [commit_2] ...

# pick up other commits to unstage (not merge)
  git cherry-pick [commit_1] --no-commit

# ------

# test clean file
  git clean -n

# clean untracked file
  git clean -f [file]

# ------

# commit
  git commit -m [new_message]

# revise the most recent commit
  git commit --amend -m [new_message]

# ------

# change commit editor
  git config --global core.editor vim

# user info setting
  git config --global user.email [email]
  git config --global user.name [name]

# list config
  git config --list

# ------

# fetch repository to a new branch
  git fetch

# git fetch + git merge
  git pull

# ------

  git init
  git add README.md
  git commit -m "first commit"
  git remote add origin [remote_repo_url]
  git push -u origin master

# ------

# push all branch
  git push --all

# delete remote branch
  git push origin [:branch_name]

# ------

# revise old commit message
  git rebase -i [commit_id]
  -> change "pick" to "reword" and then save file.

# ------

# reset to the state of previous commit and keep change to working tree
  git reset HEAD~1

# reset to commit id but keep changes to stage
  git reset --soft [commit_id]

# reset to commit id and delete all changes
  git reset --hard [commit_id]

# recover reset hard
  git reflog
  git reset --hard HEAD@{index}

# ------

# revoke commit and record history on branch
  git revert [commit_id]

# ------

# remove file
  git rm [file]

# recover file
  git checkout [file]

# ------

# stash uncommitted changes
  git stash
  git stash pop stash@{0}

# ------

# add tag to commit
  git tag [tag_name] [commit_id]

# delete local tag
  git tag -d [tag_name]

# delete remote tag
  git push origin :refs/tags/[tag_name]

# alternative approach
  git push --delete origin [tag_name]
  git tag -d [tag_name]

# ------

# list file
  git ls-files

# help
  git [command] --help

# log
  git log
  git log -10

# change file or folder name
  git mv [old_file] [new_file]

# list branch
  git branch

# add change to stage
  git add .

# check the file change
  git diff [file]

# show all change of commit
  git show [commit_id]

# check and change remote url
  git remote -v 
  git remote set-url origin [remote_repo_url]
```

### Linux

```text
# list folder info
  ls

# -l 列出詳細資料 -a 列出隱藏資料
  ls -la

# history command & filter text
  history | grep [text]

# run history id
  ![history_id]

# url
  curl [url]

# get cpu info
  lscpu

# print work directory
  pwd

# make directory
  mkdir [name]

# create file "README.md"
  touch README.md
  echo "TEST" > README.md

# copy file
  cp [file]

# move file & rename
  mv [form] [to]

# upload file to remote instance
  scp -r -i [key_path] [local_path] [remote_path]

# chmod
  chmod 777 folder

# chown
  chown owner:group folder -R

# date
  date --date=@[unix_time]

# rsync
  rsync -r --exclude [exclude_folder] [source_path] [target_path]
```

### Angular

```bash
# uninstall old version of ng cli
  sudo npm uninstall -g @angular/cli
  npm cache clean
  sudo npm install -g @angular/cli

# new a workspace
  ng new [project_name] --directory=[fold_name] --createApplication=false --interactive=false

# new an App
  ng generate application [app_name] --style=css --routing=true

# new a library
  ng generate library [library_name]

# replace package manager with yarn
  ng config -g cli.packageManager yarn
```

### AWS

```bash
# install awscli
  pip install awscli --upgrade --user

# aws configure setting
  aws configure
    AWS Access Key ID: [access_key_id]
    AWS Secret Access Key: [private_key]
    Default region name: us-west-1
    Default output format: json

# list s3 bucket
  aws s3 ls

# list contents of s3 bucket
  aws s3 ls s3://[bucket] --recursive

# copy from remote s3 bucket
  aws s3 cp s3://[bucket]/[path] [local_path] --recursive --exclude "*" --include "*.txt"

# sync folder
  aws s3 sync [local_path] s3://[bucket]/[path]
```

### Nodejs

```bash
# install nodejs
  sudo apt-get update
  curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
  sudo apt-get install -y nodejs
```

### PM2

```bash
# install pm2
  npm install pm2@latest -g

# basic command
  pm2 start
  pm2 status
  pm2 stop
  pm2 logs
  pm2 delete [process_id]

# pm2 error uv_cwd
  pm2 kill
  pm2 start pm2.config.js --env=prod -i max

# pm2 cluster
  pm2 start -i 4 --name server index.js
  pm2 start -i max index.js
```

#### pm2 env config

```javascript
  env: {
    "NODE_ENV": "develop" // pm2 start pm2.config.js
  },
  env_production: {
    "NODE_ENV": "production", // pm2 start pm2.config.js --env production
  }
```

### Reference

> **Git**
>
> * [為你自己學Git](https://gitbook.tw/)
> * [如何寫一個 Git Commit Message](https://blog.louie.lu/2017/03/21/%E5%A6%82%E4%BD%95%E5%AF%AB%E4%B8%80%E5%80%8B-git-commit-message)
> * [替專案引入規範與範例](https://wadehuanglearning.blogspot.com/2019/05/commit-commit-commit-why-what-commit.html)
> * [格式化 Git commit message — Angular format](https://medium.com/@mf99/1abb5cdbb5d9)
> * [AngularJS Git Commit Message Conventions](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#heading=h.greljkmo14y0)
>
> **Linux**
>
> * [Linux Command 命令列指令與基本操作入門教學](https://blog.techbridge.cc/2017/12/23/linux-commnd-line-tutorial/)
> * [Curl基本指令與常見用法](https://blog.techbridge.cc/2019/02/01/linux-curl-command-tutorial/)
> * [11 Console Commands](https://medium.com/better-programming/here-are-11-console-commands-every-developer-should-know-54e348ef22fa)
>
> **AWS**
>
> * [awscli docs](https://docs.aws.amazon.com/zh_tw/cli/latest/reference/)
>
> **Angular**
>
> * [angular cli docs](https://angular.io/cli)
> * [angular multi-application projects](https://octoperf.com/blog/2019/08/22/kraken-angular-workspace-multi-application-project)
>
> **Nodejs**
>
> * [pm2 docs](http://pm2.keymetrics.io/docs/usage/environment/)
> * [使用 pm2 啟動 Node.js cluster 以提升效能](https://larrylu.blog/nodejs-pm2-cluster-455ffbd7671)
> * [max-memory-restart](https://pm2.keymetrics.io/docs/usage/process-management/#max-memory-restart)


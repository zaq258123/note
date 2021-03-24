# New

#### GitLab SSH key

```bash
$ ssh-keygen -t rsa -b 4096
# generate public and private key at ~/.ssh

$ eval $(ssh-agent -s)
# 開啟 SSH agent 的指令，成功的話會回傳 Agent pid 59566

# 把 key 加到 SSH agent 的指令
$ ssh-add ~/.ssh/id_rsa

```

[git clone with SSH keys](https://tsengbatty.medium.com/bdb721bd7cf2)


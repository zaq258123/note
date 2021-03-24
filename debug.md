# Debug

### 413 Request entity too large

```bash
# edit nginx config
vi /etc/nginx/nginx.conf

# set body size
client_max_body_size 5M;

# reload service
sudo service nginx reload
```

[Request Entity Too Large](https://www.opencli.com/linux/fix-nginx-error-413-request-entity-too-large)

### EACCES permission denied

```bash
  mkdir ~/.npm-global
  
  npm config set prefix '~/.npm-global'
  
  export PATH=~/.npm-global/bin:$PATH
  
  source ~/.profile
```

 [Resolving EACCES permissions errors when installing packages globally](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally#manually-change-npms-default-directory)

### Windows 無法訪問 wsl2 localhost

### AWS DocumentDB aggregation supported error

wsl2網路與win10分開，有自己的虛擬網卡，要把虛擬網卡ip加到wsl2下的hosts

{% embed url="https://stackoverflow.com/questions/35583569/mongodb-aggregation-with-lookup-only-include-or-project-some-fields-to-return" %}

查詢wsl2下nameserver

{% embed url="https://docs.aws.amazon.com/documentdb/latest/developerguide/mongo-apis.html\#mongo-apis-aggregation-pipeline-merge" %}

```bash
cat /etc/resolv.conf
# nameserver 172.29.176.1
```



新增nameserver



```bash
sudo vi /etc/hosts
# 新增 172.18.144.1 localhost
```

[WSL2 cannot connect to localhost when the service is running on Windows](https://github.com/microsoft/WSL/issues/5211)

[https://zhuanlan.zhihu.com/p/144583887](https://zhuanlan.zhihu.com/p/144583887)


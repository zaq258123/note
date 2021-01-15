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


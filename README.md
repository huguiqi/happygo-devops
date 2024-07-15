# ansible自动化

## 执行命令
    ansible-playbook -i inventory.yaml  playbook-happygo.yaml --tags start

    ansible-playbook -i inventory.yaml  playbook-happygo.yaml --tags stop

# happygo-devops

nginx安装目录：/etc/nginx

nginx ssl目录：/etc/nginx/ssl

api微信支付证书存放目录：/home/source/certs


## 重新部署所有最新后端服务

    ansible-playbook -i inventory.yaml  playbook-happygo.yaml --tags deployAll


## 部署最新的ssl证书，并重启nginx

    ansible-playbook -i inventory.yaml  playbook-happygo.yaml --tags sslUpload


执行这个命令之前，必须将最新续签的证书下载到本机对应目录中，然后将目录地址配置到脚本上，保存后执行



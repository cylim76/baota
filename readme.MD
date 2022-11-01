'''apt update
apt install socat
apt install git'''

```
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)
```

#安装acme.sh
curl https://get.acme.sh | sh

ln -s  /root/.acme.sh/acme.sh /usr/local/bin/acme.sh

#切换CA机构, 可选： 
acme.sh --set-default-ca --server letsencrypt

#注册证书.有变更会收到邮件
acme.sh --register-account -m  xxxx@gmail.com  

#申请证书
acme.sh --issue -d 域名 --standalone

#安装证书
acme.sh --installcert -d 域名 --key-file /root/private.key --fullchain-file /root/cert.crt

# 安装X-ui   admin  admin
1.在线安装
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)

2.或本地安装
git clone https://github.com/vaxilu/x-ui
cd x-ui
bash install.sh

#面板设置

设置 证书和密钥的路径,登录x-ui面板的时候 不再提示网站不安全
/root/cert.crt
/root/private.key

建立入口(代理服务口)
- 备注
- 选择协议
-设置端口

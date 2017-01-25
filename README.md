# auto_setup_linux_rails_env

自动化安装最新linux软件脚本收集

bootstrap.sh在ubuntu中使用，Ubuntu 15.10，14.04有效

另外，生成ssh key。

``` bash
ssh-keygen -t rsa -C "your_email@example.com"
```

ruby源:

``` bash
sed -i -E 's!https?://cache.ruby-lang.org/pub/ruby!https://ruby.taobao.org/mirrors/ruby!' $rvm_path/config/db
```

pg改密码:

``` bash
ALTER USER postgres WITH PASSWORD 'postgres';
```

ubuntu 16.04安装nginx:

``` bash
# /etc/apt/sources.list
deb http://nginx.org/packages/mainline/ubuntu/ xenial nginx
deb-src http://nginx.org/packages/mainline/ubuntu/ xenial nginx
```

如果是14.04就把`xenial`换成`trusty`

``` bash
wget http://nginx.org/keys/nginx_signing.key
sudo apt-key add nginx_signing.key
sudo apt-get update
sudo apt-get install nginx
```

# Socket Server 5
docker run --detach \
--publish 1080:1080 \
--name ss5 \
--restart always \
--volume /etc/opt/ss5:/etc/opt/ss5:Z \
docker.io/zxk114/socks-server-5:latest

curl -L https://raw.githubusercontent.com/zxk114/ss5/master/ss5.conf -o /etc/opt/ss5/ss5.conf
curl -L https://raw.githubusercontent.com/zxk114/ss5/master/ss5.passwd -o /etc/opt/ss5/ss5.passwd

使用了默认端口1080，使用时只需在ss5.passwd文件更改或添加账户信息

reboot  #重启系统让配置生效

yum -y install wget

---------------------------vpn搭建------------------------------------------------------
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log


------------------------后端对接---------------------------------------------------------
curl -sSL https://get.docker.com/ | sh
   systemctl enable docker
   systemctl start docker




-------------------------------------节点------------------------------------------
docker run -d --name=ytssr -e NODE_ID=7 -e API_INTERFACE=glzjinmod -e MYSQL_HOST=149.129.77.69 -e MYSQL_USER=root -e MYSQL_DB=sspanel -e MYSQL_PASS=RG8KWmknLH6Snt7W -e SPEEDTEST=0 -e REDIRECT="" --network=host --log-opt max-size=50m --log-opt max-file=3 --restart=always 7425806/ytssr:latest


--------------------------测试运行-------------------------------------------------------
docker logs ytssr

----------------------------关闭防火墙-----------------------------------------------------
systemctl disable firewalld
iptables -X
iptables -F

mark@1143821814780949.onaliyun.com

创建用户：成功
开启控制台访问：成功
开启 Open API 调用访问：成功

r3ag0(j!CyUZX)zhANS|RdEo15uOaEbS
LTAI5tEizLhPiMDBLpCAd2f1
FiR0oI0PE4BTbNRGDgWqPpl9vb75X8
复制

阿里云域名管理
阿里云OSS管理
阿里云ECS管理

docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data -v /root/public:/public portainer/portainer-ce:linux-arm64



x86一键安装代码：docker run -d --restart=always --name="portainer" -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data 6053537/portainer-ce

arm64一键安装代码：docker run -d --restart=always --name="portainer" -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data 6053537/portainer-ce:linux-arm64


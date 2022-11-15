



## docker可视化工具：
### portainer
```shell
docker pull 6053537/portainer-ce  #直接用汉化版镜像
docker volume create portainer_data
docker run -d --name portainer -p 9000:9000 --restart=always \
     -v /var/run/docker.sock:/var/run/docker.sock \
     -v portainer_data:/data  6053537/portainer-ce
     
````

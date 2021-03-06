# itxia-docker #

## api 文档见 http://docs.itxiabacken.apiary.io/#reference

## 1. 环境依赖安装

### 安装 pip
`sudo apt-get install python-pip`

### 安装 docker 以及 docker-compose 
```
sudo apt-get -y install \
  apt-transport-https \
  ca-certificates \
  curl
```

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```
sudo add-apt-repository \
       "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
       $(lsb_release -cs) \
       stable"
```

```
sudo service docker restart
```

```
sudo apt-get update
```

```
sudo apt-get -y install docker-ce
```

```
sudo pip install docker-compose
```

### 配置 docker image repository
`curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://b9a7cc7f.m.daocloud.io`

### 下载源码
`git clone https://github.com/NJU-itxia/itxia-backend-docker.git`

### 进入文件
`cd itxia-backend-docker`

## 2. 启动服务

### 启动 docker containers
`sudo docker-compose up` 

## 3. 注意事项

### 重新启动和关闭 docker
运行 `sudo docker-compose up` 时，log 信息显示在终端界面上， 可以按 `ctrl + c` 关闭 

如果不想运行在终端界面，而是后台静默运行， 可以 `sudo docker-compose up -d` 启动 docker containers

关闭运行 `sudo docker-compose stop`

### 查看 docker containers
`sudo docker-compose ps`

或者

`sudo docker ps -a`
  

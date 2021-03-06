# 拉取镜像
## 拉取镜像命令 

```bin
gaoxinfudeMacBook-Pro:~ gaoxinfu$ docker pull zookeeper
Using default tag: latest
latest: Pulling from library/zookeeper
214ca5fb9032: Already exists 
ebf31789c5c1: Pull complete 
8741521b2ba4: Pull complete 
61e6176efc30: Pull complete 
673273952943: Pull complete 
9ac568a19196: Pull complete 
e782a6fd2e71: Pull complete 
09d9071a117c: Pull complete 
Digest: sha256:b540c5a173766064a5490e28a1ac00e94bd5f574f0288caf11352e43243a6832
Status: Downloaded newer image for zookeeper:latest
docker.io/library/zookeeper:latest
```

## 我们看列表本地镜像里已经有了zookeeper
```bin
gaoxinfudeMacBook-Pro:~ gaoxinfu$ docker images
REPOSITORY                        TAG        IMAGE ID       CREATED        SIZE
zookeeper                         latest     d3d4daa1366e   2 days ago     279MB
nginx                             latest     7425d3a7c478   3 days ago     142MB
jenkins/jenkins                   lts        73264ace1394   10 days ago    464MB
mysql                             5.7        8aa4b5ffb001   2 weeks ago    462MB
redis                             5          7891e1b96087   3 weeks ago    110MB
hanchuanchuan/goinception         latest     319c93967eed   5 weeks ago    116MB
sonatype/nexus3                   latest     b7c023b6a9b9   6 weeks ago    655MB
hhyo/archery                      v1.8.3     1f60ed35eb88   6 weeks ago    1.83GB
docker/dev-environments-default   stable-1   7c85b0303242   9 months ago   607MB
hhyo/inception                    latest     855f6b4524b7   3 years ago    688MB
```

# 启动

## 启动命令 
```bin
gaoxinfudeMacBook-Pro:docker gaoxinfu$ pwd
/Users/gaoxinfu/data/docker/zookeeper
gaoxinfudeMacBook-Pro:docker gaoxinfu$ docker run -d -e TZ="Asia/Shanghai" -p 2181:2181 -v /Users/gaoxinfu/data/docker/zookeeper:/data --name zookeeper --restart always zookeeper
11ddfc1283f0953c9372021d63490d316a4294f736829e28b600a1e6c2d2d460
```

## 命令说明 
```bin
-e TZ="Asia/Shanghai" # 指定上海时区 
-d # 表示在一直在后台运行容器
-p 2181:2181 # 对端口进行映射，将本地2181端口映射到容器内部的2181端口
--name # 设置创建的容器名称
-v # 将本地目录(文件)挂载到容器指定目录；--restart always #始终重新启动zookeeper
```

## 查看是否启动成功

```bin
gaoxinfudeMacBook-Pro:docker gaoxinfu$ docker ps
CONTAINER ID   IMAGE                 COMMAND                  CREATED          STATUS          PORTS                                                  NAMES
11ddfc1283f0   zookeeper             "/docker-entrypoint.…"   32 seconds ago   Up 28 seconds   2888/tcp, 3888/tcp, 0.0.0.0:2181->2181/tcp, 8080/tcp   zookeeper
ba2fe88dff5d   jenkins/jenkins:lts   "/sbin/tini -- /usr/…"   13 hours ago     Up 9 hours      50000/tcp, 0.0.0.0:8090->8080/tcp                      jenkins
952ef07e646e   sonatype/nexus3       "sh -c ${SONATYPE_DI…"   22 hours ago     Up 5 minutes    0.0.0.0:8081->8081/tcp                                 nexus3
gaoxinfudeMacBook-Pro:docker gaoxinfu$ 
```


# 连接
**连接工具【prettyZoo mac版本】如果需要可以留言 
## 连接配置
<img width="1035" alt="image" src="https://user-images.githubusercontent.com/26900268/168450417-1223930b-d727-4fcf-96d5-03937e6e1e25.png">
## 连接成功
<img width="1108" alt="image" src="https://user-images.githubusercontent.com/26900268/168450421-d2ea605d-de9a-4768-829f-a894a0275fe1.png">







# 拉取镜像

```java
gaoxinfudeMacBook-Pro:nexus gaoxinfu$  docker pull jenkins/jenkins:lts
lts: Pulling from jenkins/jenkins
6aefca2dc61d: Pull complete 
e1108b695755: Pull complete 
4985c9eaee97: Pull complete 
8228d7831e76: Pull complete 
9519512ddfd4: Pull complete 
0733f6b69c1e: Pull complete 
b336c88402cb: Pull complete 
cb7dc9e53b9a: Pull complete 
e07562e27aae: Pull complete 
459456f5f3a7: Pull complete 
bba697df7a23: Pull complete 
fd343a6d7b0a: Pull complete 
064f97281dfa: Pull complete 
105e1c5c62b9: Pull complete 
47468e3b9259: Pull complete 
0c33547f2be5: Pull complete 
6ae3378125de: Pull complete 
Digest: sha256:3dec77ef6636c4f4068f855fb2857bd3e8942b12bdd9c7429bd64ab8bc392527
Status: Downloaded newer image for jenkins/jenkins:lts
docker.io/jenkins/jenkins:lts
```
# docker启动

```java
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker run -p 8090:8080 --name jenkins -u root -v /Users/gaoxinfu/data/docker/jenkins:/var/jenkins_home -d jenkins/jenkins:lts;
ba2fe88dff5dd4383b46eff43c0b5f83594410e0abf418e78e64ada253a36cfb
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
```

**启动可能有点慢，需要等待一下，大概2分钟 **

# 初次登录

http://localhost:8090
## 开始登录
<img width="1090" alt="image" src="https://user-images.githubusercontent.com/26900268/168421089-d72cffb1-ad6c-4cd5-b6b3-1b0cc33342a4.png">

## 输入密码

```java
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker ps
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS          PORTS                                         NAMES
ba2fe88dff5d   jenkins/jenkins:lts         "/sbin/tini -- /usr/…"   4 minutes ago    Up 4 minutes    50000/tcp, 0.0.0.0:8090->8080/tcp             jenkins
9204c1b44422   nginx                       "/docker-entrypoint.…"   30 minutes ago   Up 30 minutes   0.0.0.0:7080->80/tcp                          nginx-test
a971cf4d4b60   hhyo/archery:v1.8.3         "dockerize -wait tcp…"   39 minutes ago   Up 32 seconds   0.0.0.0:9123->9123/tcp                        archery
a609e258fa2c   hanchuanchuan/goinception   "/usr/local/bin/dumb…"   39 minutes ago   Up 39 minutes   0.0.0.0:4000->4000/tcp                        goinception
95cbe0519793   hhyo/inception              "/bin/sh -c 'nohup /…"   39 minutes ago   Up 39 minutes   6669/tcp                                      inception
952ef07e646e   sonatype/nexus3             "sh -c ${SONATYPE_DI…"   9 hours ago      Up 9 hours      0.0.0.0:8081->8081/tcp                        nexus3
29390a46d03f   mysql:5.7                   "docker-entrypoint.s…"   3 days ago       Up 38 minutes   3306/tcp, 33060/tcp, 0.0.0.0:3307->3307/tcp   29390a46d03f_mysql
72e3a9ed05ce   redis:5                     "docker-entrypoint.s…"   4 days ago       Up 39 minutes   6379/tcp                                      redis
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker exec -it ba2fe88dff5d /bin/bash
root@ba2fe88dff5d:/# cat /var/jenkins_home/secrets/initialAdminPassword
c3b52050973442018cf3531d52234da5
root@ba2fe88dff5d:/# 
```
<img width="1009" alt="image" src="https://user-images.githubusercontent.com/26900268/168421273-22bec67b-dec5-4263-a94b-c5685df52021.png">

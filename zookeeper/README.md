# 拉取镜像

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

**我们看列表本地镜像里已经有了zookeeper**
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

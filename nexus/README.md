```java
gaoxinfudeMacBook-Pro:docker gaoxinfu$ pwd
/Users/gaoxinfu/data/docker
gaoxinfudeMacBook-Pro:docker gaoxinfu$ cd nexus/
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ ls -la
total 0
drwxr-xr-x  2 gaoxinfu  staff  64  5 14 08:55 .
drwxr-xr-x  3 gaoxinfu  staff  96  5 14 08:55 ..
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ pwd
/Users/gaoxinfu/data/docker/nexus
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ pwd
/Users/gaoxinfu/data/docker/nexus
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ ls -la
total 0
drwxr-xr-x  2 gaoxinfu  staff   64  5 14 08:55 .
drwxr-xr-x  4 gaoxinfu  staff  128  5 14 08:56 ..
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker pull sonatype/nexus3
Using default tag: latest
latest: Pulling from sonatype/nexus3
3de00bb8554b: Pull complete 
c530010fb61c: Pull complete 
7702e8da5f17: Pull complete 
17eb9ed9829d: Pull complete 
43371288717f: Pull complete 
Digest: sha256:66fe12b1eb3e97bae72eb3c2c4e436499d41ff144cdfd1dcd0718df738304732
Status: Downloaded newer image for sonatype/nexus3:latest
docker.io/sonatype/nexus3:latest
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ pwd
/Users/gaoxinfu/data/docker/nexus
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ ls -la
total 0
drwxr-xr-x  2 gaoxinfu  staff   64  5 14 08:55 .
drwxr-xr-x  4 gaoxinfu  staff  128  5 14 08:56 ..
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker run -d --name nexus3 -p 8081:8081 -v /Users/gaoxinfu/data/docker/nexus:/var/nexus-data sonatype/nexus3
952ef07e646e37932556a5da515b56a57a1a19f90974b828887b2f5805e469c5
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker exec -it 550dd77a89e1 /bin/bash
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker images |grep nexus
sonatype/nexus3                   latest     b7c023b6a9b9   6 weeks ago    655MB
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker ps
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS          PORTS                                            NAMES
952ef07e646e   sonatype/nexus3             "sh -c ${SONATYPE_DI…"   15 minutes ago   Up 15 minutes   0.0.0.0:8081->8081/tcp                           nexus3
780ec32c98e4   hhyo/archery:v1.8.4         "dockerize -wait tcp…"   2 days ago       Up 48 minutes   0.0.0.0:9123->9123/tcp                           archery
29390a46d03f   mysql:5.7                   "docker-entrypoint.s…"   2 days ago       Up 48 minutes   3306/tcp, 33060/tcp, 0.0.0.0:3307->3307/tcp      mysql
e862cde455ec   hanchuanchuan/goinception   "/usr/local/bin/dumb…"   3 days ago       Up 48 minutes   0.0.0.0:4000->4000/tcp                           goinception
72e3a9ed05ce   redis:5                     "docker-entrypoint.s…"   4 days ago       Up 48 minutes   6379/tcp                                         redis
0c7efa861338   saturn/saturn-console       "java -DSATURN_CONSO…"   9 days ago       Up 48 minutes   0.0.0.0:2181->2181/tcp, 0.0.0.0:9088->9088/tcp   saturn_console
80d9b9056e6d   saturn/saturn-db            "docker-entrypoint.s…"   9 days ago       Up 48 minutes   33060/tcp, 0.0.0.0:3308->3306/tcp                saturn_db
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker ps |grep nexus
952ef07e646e   sonatype/nexus3             "sh -c ${SONATYPE_DI…"   16 minutes ago   Up 16 minutes   0.0.0.0:8081->8081/tcp                           nexus3
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker exec -it 952ef07e646e  /bin/bash
bash-4.4$ vi /nexus-data/admin.password
bash-4.4$ vi /nexus-data/admin.password
```

**浏览器打开**
<img width="1431" alt="image" src="https://user-images.githubusercontent.com/26900268/168405969-b358e5a4-ddbd-4e86-9384-2647213848ea.png">

**登录后**
<img width="1352" alt="image" src="https://user-images.githubusercontent.com/26900268/168406003-ec2dd3e4-d0ff-46e5-b8fa-2bfd32e2a81f.png">


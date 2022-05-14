

```java
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
214ca5fb9032: Pull complete 
f0156b83954c: Pull complete 
5c4340f87b72: Pull complete 
9de84a6a72f5: Pull complete 
63f91b232fe3: Pull complete 
860d24db679a: Pull complete 
Digest: sha256:2c72b42c3679c1c819d46296c4e79e69b2616fa28bea92e61d358980e18c9751
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker images
REPOSITORY                        TAG        IMAGE ID       CREATED        SIZE
nginx                             latest     7425d3a7c478   3 days ago     142MB
saturn/demo-init                  latest     ae1d84e59360   9 days ago     674MB
saturn/saturn-console             latest     c6117ac9e7b5   9 days ago     691MB
saturn/saturn-db                  latest     6baa6dfd0f57   9 days ago     462MB
hhyo/archery                      v1.8.4     83017646f278   10 days ago    1.88GB
mysql                             5.7        8aa4b5ffb001   2 weeks ago    462MB
mysql                             latest     96d0eae5ed60   2 weeks ago    524MB
redis                             5          7891e1b96087   3 weeks ago    110MB
hanchuanchuan/goinception         latest     319c93967eed   5 weeks ago    116MB
sonatype/nexus3                   latest     b7c023b6a9b9   6 weeks ago    655MB
hhyo/archery                      v1.8.3     1f60ed35eb88   6 weeks ago    1.83GB
docker/dev-environments-default   stable-1   7c85b0303242   9 months ago   607MB
hhyo/inception                    latest     855f6b4524b7   3 years ago    688MB
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker images |grep nginx
nginx                             latest     7425d3a7c478   3 days ago     142MB
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker run --name nginx-test -p 8080:80 -d nginx
b181eadfe65d0eff4664d7ce36b903e933a32db91027fa4e781167094cba5d5c
docker: Error response from daemon: Ports are not available: listen tcp 0.0.0.0:8080: bind: address already in use.
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ sudo lsof -i tcp:8080
Password:
COMMAND PID     USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
java    629 gaoxinfu   44u  IPv6 0x1d99a03fbef62d27      0t0  TCP *:http-alt (LISTEN)
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ sudo lsof -i tcp:7080:80 -d nginx
lsof: unacceptable port specification in: -i tcp:7080:80
lsof 4.91
 latest revision: ftp://lsof.itap.purdue.edu/pub/tools/unix/lsof/
 latest FAQ: ftp://lsof.itap.purdue.edu/pub/tools/unix/lsof/FAQ
 latest man page: ftp://lsof.itap.purdue.edu/pub/tools/unix/lsof/lsof_man
 usage: [-?abhlnNoOPRtUvVX] [+|-c c] [+|-d s] [+D D] [+|-f[cgG]]
 [-F [f]] [-g [s]] [-i [i]] [+|-L [l]] [+|-M] [-o [o]] [-p s]
 [+|-r [t]] [-s [p:s]] [-S [t]] [-T [t]] [-u s] [+|-w] [-x [fl]] [--] [names]
Use the ``-h'' option to get more help information.
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker run --name nginx-test -p 7080:80 -d nginx
docker: Error response from daemon: Conflict. The container name "/nginx-test" is already in use by container "b181eadfe65d0eff4664d7ce36b903e933a32db91027fa4e781167094cba5d5c". You have to remove (or rename) that container to be able to reuse that name.
See 'docker run --help'.
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker run --name nginx-test -p 7080:80 -d nginx
9204c1b44422779a116334b7c1aaca7106dc9b84b509c80d784b91ced69b0eaa
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
```


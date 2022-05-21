

# 镜像 拉取与启动 

```javascript
gaoxinfudeMacBook-Pro:~ gaoxinfu$ docker pull memcached

Using default tag: latest
latest: Pulling from library/memcached
214ca5fb9032: Already exists 
fae8d4b1feab: Pull complete 
6dc491b9af67: Pull complete 
c355a147dff0: Pull complete 
f0cc0d566fb2: Pull complete 
98d5c91075c8: Pull complete 
Digest: sha256:71497190ee14335da71cdb6781632d330050c9e79b23a3db98e3a23bedb7b82f
Status: Downloaded newer image for memcached:latest
docker.io/library/memcached:latest
gaoxinfudeMacBook-Pro:~ gaoxinfu$ 
gaoxinfudeMacBook-Pro:~ gaoxinfu$ docker run -p 11211:11211 --name memcache memcached
```





参考地址



https://www.jianshu.com/p/950778eab529
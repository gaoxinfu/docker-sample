# 拉取镜像

```bin
gaoxinfudeMacBook-Pro:redis gaoxinfu$ docker pull redis
Using default tag: latest
latest: Pulling from library/redis
Digest: sha256:ad0705f2e2344c4b642449e658ef4669753d6eb70228d46267685045bf932303
Status: Image is up to date for redis:latest
docker.io/library/redis:latest
gaoxinfudeMacBook-Pro:redis gaoxinfu$ 
```
# 下载自己本地的redis.conf文件
http://www.redis.cn/download.html

<img width="1110" alt="image" src="https://user-images.githubusercontent.com/26900268/168451439-3cfe65c0-9bdb-4c1a-8a93-5a1869338a8c.png">
**将这个文件 可以复制到自己的自定义的目录下，以后改这个文件配置即可**
<img width="1067" alt="image" src="https://user-images.githubusercontent.com/26900268/168451450-cb8493d3-f918-4949-96b8-437b5fdee897.png">
<img width="1143" alt="image" src="https://user-images.githubusercontent.com/26900268/168451469-65de7f8c-72e2-454d-b456-df02c256e311.png">

**修改redis.conf的三个重要配置**

```bin
 # bind 127.0.0.1 #注释掉这部分，使redis可以外部访问
 protected-mode no
 appendonly yes 
```
<img width="993" alt="image" src="https://user-images.githubusercontent.com/26900268/168451423-638fde67-8c6f-4b31-beb2-b49972403b23.png">

<img width="750" alt="image" src="https://user-images.githubusercontent.com/26900268/168451548-8078cbb8-b5a4-4b31-bc6e-111063744bb5.png">

<img width="1049" alt="image" src="https://user-images.githubusercontent.com/26900268/168451555-6b38c41f-453f-4646-bd35-7aeefca7ff3f.png">

# 启动

```bin
gaoxinfudeMacBook-Pro:redis gaoxinfu$ docker run -p 6379:6379 --name redis -v /Users/gaoxinfu/data/docker/redis/redis.conf:/etc/redis/redis.conf  -v /Users/gaoxinfu/data/docker/redis/data:/data -d redis redis-server /etc/redis/redis.conf --appendonly yes
87cda61aff660a765e0df37ef3be05b8ae879c45e6544e23d242fb8431442a6c
gaoxinfudeMacBook-Pro:redis gaoxinfu$ 
```

# 连接

## 连接工具：D-dis
<img width="376" alt="image" src="https://user-images.githubusercontent.com/26900268/168451588-2e1e6f91-ee68-47c4-958c-7313f585873f.png">

## 连接配置
<img width="735" alt="image" src="https://user-images.githubusercontent.com/26900268/168451562-1f21c6cb-a2ef-4a1c-b4a8-74551c3eddd8.png">

<img width="1070" alt="image" src="https://user-images.githubusercontent.com/26900268/168451594-0fec0a32-68c5-4a90-a416-edbea3ed379f.png">

<img width="735" alt="image" src="https://user-images.githubusercontent.com/26900268/168451562-1f21c6cb-a2ef-4a1c-b4a8-74551c3eddd8.png">



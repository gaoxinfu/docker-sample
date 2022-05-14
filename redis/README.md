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
**修改重要的一个可以访问的配置,**
 bind 127.0.0.1 #注释掉这部分，使redis可以外部访问
<img width="993" alt="image" src="https://user-images.githubusercontent.com/26900268/168451423-638fde67-8c6f-4b31-beb2-b49972403b23.png">

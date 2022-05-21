

docker pull fuyong/treenms 



```java
gaoxinfudeMacBook-Pro:~ gaoxinfu$ docker pull fuyong/treenms
Using default tag: latest
latest: Pulling from fuyong/treenms
d660b1f15b9b: Pull complete 
46dde23c37b3: Pull complete 
ac5ffaa94f61: Pull complete 
f7e9f30394f5: Pull complete 
3ae3a41d5873: Pull complete 
8eea330fdc65: Pull complete 
d051bc095250: Pull complete 
d4f397a5ced6: Pull complete 
8b01e0b079d4: Pull complete 
e63b68df2293: Pull complete 
e045242e6369: Pull complete 
7b620a0e2a41: Pull complete 
3f6a7a3f2d21: Pull complete 
Digest: sha256:97790f5ece960ddf2e5ee4cfb87feb1066f87947efeaed0fd2733625cd1cec51
Status: Downloaded newer image for fuyong/treenms:latest
docker.io/fuyong/treenms:latest
gaoxinfudeMacBook-Pro:~ gaoxinfu$ 
gaoxinfudeMacBook-Pro:~ gaoxinfu$ docker run \
> --restart=always \
> -p 8070:8070 --name treenms-web -d \
> fuyong/treenms:latest
36f55c0f7d25d6761f385ff542c63d0442371a05db77871915a148ec2b5772f9  
```



```bash
docker run \
--restart=always \
-p 8070:8070 --name treenms-web -d \
fuyong/treenms:latest
```

参考地址



https://hub.docker.com/r/fuyong/treenms


# 主要是参考下面的地址进行搭建

https://www.jianshu.com/p/5fc4ad130edc

```bin
gaoxinfudeMacBook-Pro:oracle gaoxinfu$ pwd
/Users/gaoxinfu/data/docker/oracle
gaoxinfudeMacBook-Pro:oracle gaoxinfu$ docker run \
> --privileged \
> --restart=always \
> --name oracle_11g \
> -v /Users/gaoxinfu/data/docker/oracle/:/home/oracle/app/oracle/flash_recovery_area/ \
> -p 1521:1521 \
> -d registry.cn-hangzhou.aliyuncs.com/helowin/oracle_11g
;
```

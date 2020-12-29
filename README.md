# nanoserver

![](https://mmbiz.qpic.cn/mmbiz_png/hD75vrNauXamKWicHJbMPjDic7D1zTAW8G0L25Ybv7BMbwHe3dcnC37icqpVEkDQaemfNYma0wI4N5ia2tAib6rNHsQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

我是为少！我的微信是：uuhells123，公众号：黑客下午茶

这是为了学习 fork 的项目，源项目地址是：[nanoserver](https://github.com/lonng/nanoserver)

我弄的完整调试教程：[探索 Golang 云原生游戏服务器开发，硬核实战之调试 NanoServer 生产级麻将游戏服务器](https://mp.weixin.qq.com/s/jAj0lh57NflZQsi5cw5xMw)

# docker compose 本地调试或二次开发

**清理数据**

```sh
docker volume ls
docker volume rm nanoserver_db_data
```

**启动 mysql & adminer**

```sh
docker-compose -f docker-compose.mysql.yaml up
# docker-compose -f docker-compose.mysql.yaml down
```

**Detached mode: Run containers in the background**

```sh
docker-compose -f docker-compose.mysql.yaml up -d
docker-compose -f docker-compose.mysql.yaml ps
```

进入：[http://localhost:8086/](http://localhost:8086/)，管理数据库

**启动服务器**

开发：

```sh
docker-compose -f docker-compose.dev.yaml up scmj
# docker-compose -f docker-compose.dev.yaml down
```

调试：

```sh
docker-compose -f docker-compose.dev.yaml up scmj-debug
# docker-compose -f docker-compose.dev.yaml down
```

## Drone CI/CD + K8S =>> DevOps

[生产级Golang麻将游戏服务器 NanoServer 二次开发，利用Drone CI/CD打通DevOps上 K8S 迭代流程](https://mp.weixin.qq.com/s?__biz=MzA4Mzc4NTE5MQ==&mid=2692293281&idx=1&sn=251610f58fdde69cb47bbf62bce6403b&chksm=ba7ca6298d0b2f3ff77d5f43151f7e38a0ad4345de43a295d377b28feb9eb76010441c779e76&token=184248889&lang=zh_CN#rd)

![](https://mmbiz.qpic.cn/mmbiz_png/hD75vrNauXamKWicHJbMPjDic7D1zTAW8G5JBk778BCr4XVnTfLqrlbRibVGUQRS5SriaxkTiax8W9EpVSHL01ps3Kw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![](https://mmbiz.qpic.cn/mmbiz_png/hD75vrNauXamKWicHJbMPjDic7D1zTAW8G15iaicumHl7ZPJ8TWSaBUsqdlzqTn9D5nUcbnpU4VGtHETnN5SkOpxRw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
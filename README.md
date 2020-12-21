# nanoserver

这是为了学习 fork 的项目，源地址是：[nanoserver](https://github.com/lonng/nanoserver)

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
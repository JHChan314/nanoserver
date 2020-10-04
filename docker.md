### DEV

```sh
## mysql & adminer
docker-compose -f docker-compose.mysql.yaml up -d

docker build -f Dockerfile.dev -t scmj-server:dev .

docker-compose -f docker-compose.dev.yaml up scmj
```
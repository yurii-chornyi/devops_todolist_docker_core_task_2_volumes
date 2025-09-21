1. Run MySQL Container
Run the MySQL container with a volume attached:
`
docker build -t mysql-local:1.0.0 -f Dockerfile.mysql .
docker network create todolist-net
docker run -d \
  --name mysql-local \
  --network todolist-net \
  -v mysql-data:/var/lib/mysql \
  -p 3306:3306 \
  mysql-local:1.0.0

`

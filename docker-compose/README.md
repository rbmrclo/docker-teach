# Cheatsheet

- Enter `docker-compose.yml`
- A tool that lets you compose together multiple docker containers
- Tool for development and production

```bash
$ docker-compose build
$ docker-compose up
$ docker-compose stop

$ docker-compose up --build -d # background
$ docker-compose ps
$ docker-compose logs -f
$ docker-compose restart
$ docker-compose restart redis
$ docker-compose exec web ls -la # run a command in an already running container
$ docker-compose exec web sh
$ docker-compose run redis redis-server --version

$ docker-compose rm
```

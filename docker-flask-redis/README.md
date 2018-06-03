# Cheatsheet

```bash
$ docker network ls
$ docker network inspect bridge
$ docker network create --driver bridge firstnetwork

$ docker exec web2 ifconfig
$ docker exec web2 ping 172.17.0.2
$ docker exec redis cat /etc/hosts

$ docker container run --rm -itd -p 6379:6379 --name redis redis:3.2-alpine
$ docker container run --rm -itd -p 5000:5000 -e FLASK_APP=app.py -e FLASK_DEBUG=1 --name web2 -v $PWD:/app web2
$ docker container stop web2
$ docker container stop redis

$ docker container run --rm -itd -p 6379:6379 --name redis --net firstnetwork redis:3.2-alpine
$ docker container run --rm -itd -p 5000:5000 -e FLASK_APP=app.py -e FLASK_DEBUG=1 --name web2 -v $PWD:/app --net firstnetwork web2
```

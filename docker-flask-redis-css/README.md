# Cheatsheet

The goal of this lesson is to become familiar on how to share data between containers.

```bash
$ docker container run --rm -itd -p 5000:5000 -e FLASK_APP=app.py -e FLASK_DEBUG=1 --name web2 -v $PWD:/app web2
$ docker container run --rm -itd -p 6379:6379 --name redis --net firstnetwork -v web2_redis:/data --volumes-from web2 redis:3.2-alpine

$ docker container exec -it redis sh
```

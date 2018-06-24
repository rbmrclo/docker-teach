# Cheatsheet

The goal of this lesson is to become familiar with docker entrypoint where we
could run scripts when a container starts.

```bash
$ docker container run --rm -itd -p 6379:6379 --name redis --net firstnetwork -v web2_redis:/data redis:3.2-alpine
$ docker image build -t webentrypoint .
$ docker container run --rm -it -p 5000:5000 -e FLASK_APP=app.py -e FLASK_DEBUG=1 --name webentrypoint -v $PWD:/app --net firstnetwork webentrypoint

# Visit localhost:5000

$ docker container run --rm -it -p 5000:5000 -e FLASK_APP=app.py -e FLASK_DEBUG=1 -e WEB2_COUNTER_MSG="Docker fans have visited this page." --name webentrypoint --net firstnetwork webentrypoint
```

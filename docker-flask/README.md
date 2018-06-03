# Cheatsheet

```bash
$ docker image ls
$ docker image build -t web1 .
$ docker image push rbmrclo/web1:latest
$ docker image rm -f [4-char-hash]

$ docker pull rbmrclo/web1:latest

$ docker container ls
$ docker container rm [4-char-hash|name]
$ docker container run -it -p 5000:5000 -e FLASK_APP=app.py web1                                     # basic
$ docker container run -it --rm --name web1 -p 5000:5000 -e FLASK_APP=app.py web1                    # autodestroy
$ docker container run -it --rm --name web1 -p 5000:5000 -e FLASK_APP=app.py -d web1                 # daemonized
$ docker container run -it --name web2 -p 5000:5000 -e FLASK_APP=app.py -d --restart on-failure web1 # restart onfailure
$ docker container logs [4-char-hash|name]
$ docker container stats
$ docker container stop web1
$ docker container exec -it web1 flash --version

# Livereload with mounting volumes
$ docker container run -it -p 5000:5000 -e FLASK_APP=app.py --rm --name web1 -e FLASK_DEBUG=1 -v $PWD:/app web1

# Test with other languages (challenge)
$ docker container run -it --rm --name testpython python:2.7-alpine python
```
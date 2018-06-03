# Cheatsheet

```bash
$ docker image ls
$ docker image build -t web1 .
$ docker image push rbmrclo/web1:latest
$ docker image rm -f [4-char-hash]

$ docker pull rbmrclo/web1:latest

$ docker container run -it -p 5000:5000 -e FLASK_APP=app.py web1
```
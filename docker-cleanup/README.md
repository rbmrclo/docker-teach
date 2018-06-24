# Cheatsheet

```
$ docker container ls
$ docker system df

# Can be safely removed
$ docker container ls -a

# All with <none> are dangling, completely safe to delete
$ docker image ls

# Debugging / Verify if docker is installed correctly
$ docker system info

# You can also set it as a cron job
$ docker system prune
$ docker system prune -a # dangerous
$ docker system prune -f # force

$ docker container stop <container_names separated by space>
$ docker container stop $(docker container ls -a -q)
```

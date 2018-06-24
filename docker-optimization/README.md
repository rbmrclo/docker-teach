# Cheatsheet

The goal of this lession is to perform shrinkage in your docker image.

```bash
$ docker image build -t weboptimized .
$ docker image ls # check that the weboptimized is smaller
```

#### `.dockerignore`

```
# Blacklist

.dockerignore
.git/
.foo/*
**/*.swp
**/*.txt
!special.txt

# Whitelist

!Dockerfile
```

#### Downside

- Though the image is smaller, it needs to install packages again and again even without changes
- Non-optimized is still efficient

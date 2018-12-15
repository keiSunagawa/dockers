## build
```
docker build -t amm .
```

## run
```
# make container
$ docker run -it --name scala_repl amm bash

# dettach
C-p C-q

# attach
$ docker attach scala_repl
```
TODO mount host [scala & sbt cache] dir

# Creating refnet client on docker:
#### Cloning the repository

build the docker from github
```sh
$ docker build --tag "refnet" https://github.com/natangl/refnet.git
```

##### Now run the image in the background
```sh
$ docker run -td --name refnet -p 11332:11332 -p 21332:21332 -p 21443:21443 -p 11334:11333 docker_id
```

#### And to run a bash terminal inside the docker:
```sh
$ docker exec -it refnet /bin/bash
```

# Building and running the Cpuminer docker:

### Building:
```sh
$ docker build --tag "miner" https://github.com/natangl/cpuminer-multi.git
```

### Running:

```sh
$ docker run -td --name miner -p <rpcport>:<rpcport> docker_image
$ docker exec -it miner /bin/bash
$ ./cpuminer -o http://<the ip to connect>:<rpcport> -O <yourpcuser>:<yourrpcpassword> -a sha256d --no-longpoll --no-getwork --coinbase-addr=<the address to which you want to mine>
```

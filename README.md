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

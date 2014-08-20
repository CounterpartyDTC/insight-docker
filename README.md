## Build

    git clone https://github.com/Dogeparty/insight-doge-api.git
    cd insight-doge-api
    ln path/to/insight-docker/Dockerfile
    docker build -t insight-doge:v1 .

## Data

    docker run -d --name insight-doge-data insight-doge:v1 bash


## Run Container

    docker run -it --name=insight-doge --volumes-from=insight-doge-data --link dogecoind:dogecoind insight-doge:v1 bash


## ENVs

    export BITCOIND_HOST=$DOGECOIND_PORT_22555_TCP_ADDR
    export BITCOIND_PORT=$DOGECOIND_PORT_22555_TCP_PORT
    export BITCOIND_P2P_PORT=$DOGECOIND_PORT_22556_TCP_PORT


## Run Process

    node insight.js


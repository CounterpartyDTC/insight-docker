## Build

    git clone https://github.com/Dogeparty/insight-doge-api.git
    cd insight-doge-api
    ln path/to/insight-docker/testnet/Dockerfile
    docker build -t insight-doge:testnet .

## Data

    docker run -d --name insight-doge-testnet-data insight-doge:testnet bash


## Run Container

    docker run -it --name=insight-doge-testnet --volumes-from=insight-doge-testnet-data --link dogecoind-testnet:dogecoind insight-doge:testnet bash


## ENVs

    export BITCOIND_HOST=$DOGECOIND_PORT_44555_TCP_ADDR
    export BITCOIND_PORT=$DOGECOIND_PORT_44555_TCP_PORT
    export BITCOIND_P2P_PORT=$DOGECOIND_PORT_44556_TCP_PORT


## Run Process

    node insight.js


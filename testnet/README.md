## Build

    git clone https://github.com/Dogeparty/insight-doge-api.git
    cd insight-doge-api
    ln path/to/insight-docker/testnet/Dockerfile
    docker build -t insight-doge:testnet .

## Data

    docker run -d --name insight-doge-testnet-data insight-doge:testnet bash


## Run Container

    docker run -it --name=insight-doge-testnet --volumes-from=insight-doge-testnet-data --link dogecoind-testnet:dogecoind insight-doge:testnet bash


## Run Process

Precondition: Make sure to have dogecoind fully synchronized.

    node insight.js


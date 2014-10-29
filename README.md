# Docker recipe for [insight-doge-api](https://github.com/Dogeparty/insight-doge-api)

See the global picture how this container interacts with other components to run Dogeparty:

[Global Component Overview](http://www.inkpad.io/1GMXYwxl4Q)


## Build

    git clone https://github.com/Dogeparty/insight-doge-api.git
    cd insight-doge-api
    ln path/to/insight-docker/Dockerfile
    docker build -t insight-doge:v1 .

## Data

    docker run -d --name insight-doge-data insight-doge:v1 bash


## Run Container

    docker run -it --name=insight-doge --volumes-from=insight-doge-data --link dogecoind:dogecoind insight-doge:v1 bash


## Run Process

    node insight.js


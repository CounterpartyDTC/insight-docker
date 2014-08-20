FROM node

# replace this with your application's default port
EXPOSE 3001

ENV HOME /root

# config
ENV NODE_ENV production
ENV BITCOIND_HOST 192.168.59.3
ENV BITCOIND_PORT 44555
ENV BITCOIND_P2P_PORT 44556
ENV BITCOIND_USER user
ENV BITCOIND_PASS pass
#ENV BITCOIND_DATADIR       # bitcoind datadir. 'testnet3' will be appended automatically if testnet is used. NEED to finish with '/'. e.g: `/vol/data/`
# [= 'livenet' | 'testnet']
ENV INSIGHT_NETWORK testnet
# Path where to store insight's internal DB. (defaults to $HOME/.insight)
ENV INSIGHT_DB /root/data
#ENV INSIGHT_SAFE_CONFIRMATIONS=6  # Nr. of confirmation needed to start caching transaction information
#ENV INSIGHT_IGNORE_CACHE  # True to ignore cache of spents in transaction, with more than INSIGHT_SAFE_CONFIRMATIONS confirmations. This is useful for tracking double spents for old transactions.

VOLUME /root/data
RUN mkdir /root/data/testnet

# replace this with your main "server" script file
CMD [ "node", "insight.js" ]

ADD . /usr/src/app
WORKDIR /usr/src/app

# install your application's dependencies
RUN npm install


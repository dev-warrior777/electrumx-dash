# example of Dockerfile that builds release of electrumx-1.13.0
# ENV variables can be overrided on the `docker run` command

FROM ubuntu:22.04

WORKDIR /
ADD https://github.com/dev-warrior777/electrumx-dash/archive/1.16.0.1.tar.gz /
RUN tar zxvf *.tar.gz

RUN apt-get update && \
        apt-get -y install python3.10 python3-pip librocksdb-dev libsnappy-dev libbz2-dev libz-dev liblz4-dev

RUN cd /electrumx-dash* && pip3 install .[rocksdb]

ENV SERVICES="tcp://:57001"
ENV COIN=Dash
ENV DB_DIRECTORY=/db
ENV DAEMON_URL="http://username:password@hostname:port/"
ENV ALLOW_ROOT=true
ENV DB_ENGINE=rocksdb
ENV MAX_SEND=10000000
ENV BANDWIDTH_UNIT_COST=50000
ENV CACHE_MB=2000

VOLUME /db

RUN mkdir -p "$DB_DIRECTORY" && ulimit -n 1048576

CMD ["/usr/bin/python3", "/usr/local/bin/electrumx_server"]

# build it with for Example:
# `docker build -t electrumx_dash .`
#
# run it with for Example:
# `docker run -d --net=host -v /home/<username>/electrumx-dash/db/:/db -e DAEMON_URL="http://youruser:yourpass@localhost:9998" -e REPORT_SERVICES=tcp://example.com:50001 electrumx-dash`
#
# for a proper clean shutdown, send TERM signal to the running container eg.: `docker kill --signal="TERM" CONTAINER_ID`

#syntax=docker/dockerfile-upstream:1.4.0-rc1

FROM attemptthisonline/base

ARG PARIGP_VERSION=2.15.4

RUN curl -L https://pari.math.u-bordeaux.fr/pub/pari/unix/pari-$PARIGP_VERSION.tar.gz | \
    tar -xz && \
    cd pari-$PARIGP_VERSION && \
    ./Configure --mt=pthread && \
    make all -j $(nproc) && \
    make install && \
    cd / && \
    rm -rf /tmp/pari-$PARIGP_VERSION

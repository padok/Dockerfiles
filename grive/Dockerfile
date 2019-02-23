FROM ubuntu:16.04
RUN apt-get update \
    && apt-get install -y git cmake build-essential libgcrypt11-dev libyajl-dev \
                          libboost-all-dev libcurl4-openssl-dev libexpat1-dev libcppunit-dev binutils-dev \
                          debhelper zlib1g-dev dpkg-dev pkg-config \
    && rm -rf /var/cache/apt/archives /var/lib/apt/lists/*


WORKDIR /grive-source/

RUN git clone https://github.com/vitalif/grive2 ./

RUN mkdir build \
    && cd build \
    && cmake ..

WORKDIR /grive-source/build/

RUN make -j4 \
    && make install

WORKDIR /grive-source/

RUN mkdir sync-folder



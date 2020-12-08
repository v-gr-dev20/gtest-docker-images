FROM gcc-l:latest

WORKDIR /usr/src/cmake.git

RUN apt-get update \
 && apt-get install -y git \
 && git clone https://gitlab.kitware.com/cmake/cmake.git /usr/src/cmake.git \
 && ./bootstrap && make && make install && rm -Rf /usr/src/cmake.git

WORKDIR /
FROM gcc-gdb-locales:latest

WORKDIR /usr/src/cmake.git

RUN apt -y update \
 && apt -y install git \
 && git clone https://gitlab.kitware.com/cmake/cmake.git /usr/src/cmake.git \
 && ./bootstrap \
 && make \
 && make install \
 && rm -Rf /usr/src/cmake.git

WORKDIR /
ARG build_type=Release
FROM cmake:latest

WORKDIR /

RUN apt -y update \
 && apt -y install libboost-dev libboost-program-options-dev \
 && git clone https://github.com/google/googletest.git -b release-1.11.0 \
 && cd googletest \
 && mkdir build \
 && cd build \
 && cmake -DCMAKE_BUILD_TYPE=$build_type .. \
 && cmake --build . \
 && make install \
 && cd / \
 && rm -Rf /googletest

WORKDIR /sources
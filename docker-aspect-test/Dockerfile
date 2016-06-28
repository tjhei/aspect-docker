FROM tjhei/dealii:v8.4.1

MAINTAINER timo.heister@gmail.com

ARG VER=master

USER bob

# get repo
RUN git clone https://github.com/geodynamics/aspect.git && cd aspect && git checkout $VER

# build
RUN cd aspect && mkdir build && cd build && cmake .. && make -j 8 && make test

RUN ln -s ~/aspect/build/aspect aspect/

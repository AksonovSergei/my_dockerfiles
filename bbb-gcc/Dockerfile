#######################################################
# Dockerfile for the Beaglebone blue cross compilation
#######################################################

FROM debian:buster

RUN apt-get update -q && \
    DEBIAN_FRONTEND=noninteractive && \
    apt-get install -y -q \
    gcc-8-arm-linux-gnueabihf

ENV HOST=arm-linux-gnueabihf \
    CROSS_ROOT_BINDIR=/usr/bin

ENV ARCH=arm \
    CROSS_COMPILE=${CROSS_ROOT_BINDIR}/${HOST}- \
    ARM_CROSS_COMPILER=TRUE

ENV AS=${CROSS_COMPILE}as \
    AR=${CROSS_COMPILE}ar \
    CC=${CROSS_COMPILE}gcc \
    CPP=${CROSS_COMPILE}cpp \
    CXX=${CROSS_COMPILE}g++ \
    LD=${CROSS_COMPILE}ld

WORKDIR /build

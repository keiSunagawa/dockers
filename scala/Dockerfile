FROM ubuntu:16.04

# Install JDK, misc packages.
RUN apt-get update && apt-get install -y \
    default-jdk \
    apt-transport-https \
    curl

# Install sbt. See http://www.scala-sbt.org/1.0/docs/Installing-sbt-on-Linux.html
RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
RUN apt-get update && apt-get install -y sbt 

# RUN: docker buildするときに実行される
# RUN curl -L https://github.com/lihaoyi/Ammonite/releases/download/1.5.0/2.12-1.5.0 > /usr/local/bin/amm && chmod +x /usr/local/bin/amm && mkdir /root/.ammonite

# Install ammonite. See http://ammonite.io/#Ammonite-REPL
RUN curl -L -o /usr/bin/amm https://git.io/vdNv2 && chmod +x /usr/bin/amm && mkdir /root/.ammonite

RUN export TERM=vt100
RUN mkdir -p ~/scala/src

# CMD: docker runするときに実行される
CMD bash


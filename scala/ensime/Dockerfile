FROM scala

RUN yum -y install ctags git

# settings
RUN mkdir -p ~/.sbt/1.0/plugins \
        && echo 'addSbtPlugin("org.ensime" % "sbt-ensime" % "2.5.1")' >> ~/.sbt/1.0/plugins/plugins.sbt \
        && echo 'alias ensime="ctags -Re . & sbt clean ensimeConfig test:compile ensimeServerIndex"' >> ~/.bashrc

RUN mkdir -p /home/kerfume/scala/src

RUN git clone https://github.com/keiSunagawa/ensime-server.git \
        && cd ensime-server \
        && git checkout in-docker \
        && sbt "project server" publishM2

RUN echo 'ensimeServerVersion := "2.0.2+1-15ca6536-SNAPSHOT"' >> ~/.sbt/1.0/build.sbt \
        && echo 'ensimeProjectServerVersion := "2.0.2+1-15ca6536-SNAPSHOT"' >> ~/.sbt/1.0/build.sbt

EXPOSE 6000
EXPOSE 6001

CMD bash

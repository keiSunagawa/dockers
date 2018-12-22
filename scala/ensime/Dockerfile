FROM scala

RUN yum -y install ctags

# settings
RUN mkdir -p ~/.sbt/1.0/plugins \
        && echo 'addSbtPlugin("org.ensime" % "sbt-ensime" % "2.5.1")' >> ~/.sbt/1.0/plugins/plugins.sbt \
        && echo 'alias ensime="ctags -Re . & sbt clean ensimeConfig test:compile ensimeServerIndex"' >> ~/.bashrc

RUN mkdir -p ~/scala/src

CMD bash

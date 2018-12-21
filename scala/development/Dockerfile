FROM scala

# settings
RUN mkdir -p ~/.sbt/1.0/plugins \
        && echo 'addSbtPlugin("org.ensime" % "sbt-ensime" % "2.5.1")' >> ~/.sbt/1.0/plugins/plugins.sbt \
        && echo 'alias ensime2="ctags -Re . & sbt clean ensimeConfig test:compile ensimeServerIndex"' >> ~/.bashrc

# TODO install emacs

RUN mkdir ~/.emacs.d

CMD bash


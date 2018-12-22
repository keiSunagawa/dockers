FROM centos:7

# Install JDK.
RUN yum -y install java-1.8.0-openjdk \
        java-1.8.0-openjdk-javadoc \
        java-1.8.0-openjdk-src \
        java-1.8.0-openjdk-headless \
        java-1.8.0-openjdk-devel \
        java-1.8.0-openjdk-demo \
        java-1.8.0-openjdk-accessibility \
        && export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.144-0.b01.el7_4.x86_64 \
        && export PATH=$PATH:$JAVA_HOME/bin \
        && export CLASSPATH=.:$JAVA_HOME/jre/lib:$JAVA_HOME/lib:$JAVA_HOME/lib/tools.jar

# Install sbt. See http://www.scala-sbt.org/1.0/docs/Installing-sbt-on-Linux.html
RUN curl https://bintray.com/sbt/rpm/rpm | tee /etc/yum.repos.d/bintray-sbt-rpm.repo \
        && yum install -y sbt

CMD bash

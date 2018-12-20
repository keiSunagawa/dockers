FROM centos:7

# dependencies
RUN yum install -y gcc make wget \
        giflib-devel \
        libjpeg-devel \
        libpng-devel \
        libtiff-devel \
        gtk2-devel \
        libXaw-devel \
        ncurses-devel \
        libxml2-devel \
        libotf-devel \
        gnutls-devel \
        libselinux-devel \
        librsvg2-devel \
        dbus-devel \
        gpm-devel \
        GConf2-devel \
        m17n-lib-devel \
        libXft-devel

# install emacs
RUN cd /usr/local/src \
        && wget http://ftp.gnu.org/pub/gnu/emacs/emacs-26.1.tar.gz \
        && tar zxvf emacs-26.1.tar.gz \
        && cd emacs-26.1 && ./configure --without-x && make && make install

CMD bash

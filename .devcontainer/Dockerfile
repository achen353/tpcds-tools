FROM        ubuntu:jammy-20220801
LABEL       version="1.0"
ENV         DEBIAN_FRONTEND noninteractive

# update and install dependencies
RUN   apt-get -y update && apt-get -y install build-essential \
      && apt-get -y install gcc-9 g++-9 gcc-10 g++-10 \
      && update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 9 \
      && update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-9 9 \
      && update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-10 10 \
      && update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-10 10 \
      && apt-get -y install zip unzip git zsh curl git-all \
      && apt-get -y install openjdk-8-jdk maven mysql-server \
      && apt-get -y install python3 python3-pip

RUN   sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" --unattended
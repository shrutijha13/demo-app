FROM jenkins/jenkins:lts
USER root
RUN  apt-get update && apt-get install  -y maven
RUN  apt-get install -y software-properties-common
RUN  add-apt-repository ppa:ethereum/ethereum
RUN  apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 1C52189C923F6CA9
RUN  apt-get update
RUN  apt-get install -y  solc
FROM ubuntu:16.04

RUN apt-get update && apt-get -y install maven openjdk-8-jdk-headless openssh-server git
RUN useradd jenkins

RUN mkdir -p /home/jenkins/.ssh/ /var/run/sshd

RUN chown jenkins -R /home/jenkins 
USER jenkins

COPY authorized_keys /home/jenkins/.ssh/
USER root

EXPOSE 22
CMD ["/usr/sbin/sshd","-D" ]


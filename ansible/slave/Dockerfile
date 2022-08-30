FROM centos:centos7

# Update the index of available packages.
RUN yum update -y

# Install the requires package.
RUN yum install -y net-tools.x86_64 openssh-server openssh-clients python sudo curl wget bash-completion openssl && yum clean all

# Setting the root password
RUN echo 'root:root' | chpasswd

# Generate the ssh host keys.
RUN ssh-keygen -A

EXPOSE 22

# Run ssh server daemon.
CMD ["/usr/sbin/sshd", "-D"]

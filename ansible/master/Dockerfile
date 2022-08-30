FROM centos:centos7

# # 通过pip安装ansiblle
ENV LANG=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8

# Update the index of available packages.
RUN yum update -y

# Install the requires package.
RUN yum install -y net-tools.x86_64 openssh-server openssh-clients python sudo curl wget bash-completion openssl && yum clean all

# Install ansible 
RUN pip install --upgrade pip && pip install -i https://pypi.tuna.tsinghua.edu.cn/simple ansible

# Setting the root password
RUN echo 'root:root' | chpasswd

# Generate the ssh host keys.
RUN ssh-keygen -A

# Generate public key.ready to copy to slave server
RUN ssh-keygen -t rsa

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
FROM centos:centos7

# # 通过pip安装ansiblle
ENV LANG=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8

# Update the index of available packages.
RUN yum update -y

# Install the requires package.
RUN yum install -y net-tools.x86_64 openssh-server openssh-clients python3.x86_64 sudo curl wget bash-completion openssl sshpass && yum clean all

# Install ansible 
RUN pip3 install --upgrade pip && pip install -i https://pypi.tuna.tsinghua.edu.cn/simple ansible

# Setting the root password
RUN echo 'root:root' | chpasswd

# Generate the ssh host keys.
RUN ssh-keygen -A

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
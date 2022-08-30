# master连接slave步骤

- master生成公私钥
	- $ ssh-keygen -t rsa
- 拷贝公钥到各slave
	- $ ssh-copy-id -i /root/.ssh/id_rsa.pub root@ansible-slave1
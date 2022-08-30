### 项目介绍
此项目可用于快速搭建基于docker的练习ansible环境

#### 运行步骤
- 进入ansible目录
- 运行命令: $ docker-compose up -d
- 通过ssh工具登录到master，生成公私钥：$ ssh-keygen -t rsa
- 拷贝公钥到slave：$ ssh-copy-id -i /root/.ssh/id_rsa.pub root@ansible-slave
- 测试ssh连接是否正常:$ ssh root@ansible-slave
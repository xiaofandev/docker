### 项目介绍
此项目可用于快速搭建基于docker的练习ansible环境

#### 运行步骤
1. 进入ansible目录
2. 运行命令: $ docker-compose up -d
3. 通过ssh工具登录到master，生成公私钥：$ ssh-keygen -t rsa
4. 拷贝公钥到slave：$ ssh-copy-id -i /root/.ssh/id_rsa.pub root@ansible-slave
5. 测试ssh连接是否正常:$ ssh root@ansible-slave

#### 资料参考
- 《Ansible自动化运维：技术与最佳实践》
- https://www.w3cschool.cn/automate_with_ansible/



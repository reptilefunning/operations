执行命令，安装Python和flask,redis
-
~~~
ansible-playbook init_flask.yml
ansible-playbook install_zabbix.yml
~~~

复制到远端后执行脚本
-
~~~
scp centos7_install_zabbix.sh root@192.168.1.39:~
ssh root@192.168.1.39:~ "bash centos7_install_zabbix.sh"
~~~

hosts配置 centos7\ubuntu16.04
-
~~~
centos ansible_ssh_port=22 ansible_ssh_host=192.168.1.39 ansible_ssh_user=root
ubuntu ansible_ssh_port=22 ansible_ssh_host=192.168.1.19 ansible_ssh_user=root
[test]
centos
ubuntu
~~~

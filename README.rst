VAGRANT-BAE
======================

Overview
--------
vagrant-bae��һ���������⻯��������vagrant����İ��� BAE3_ ִ�е�Ԫ����ģ���Ubuntu (12.04.2 LTS)�����������
�����ڲ����� BAE3_ ����ͬ����ִ�л��������ڿ������ڱ��ص��ԡ����д��롣

Installation
-------------
1. ��װ virtualbox https://www.virtualbox.org 
2. ��װ vagrant http://www.vagrantup.com 
3. ��װ git http://git-scm.com/downloads ����(for windows) http://msysgit.github.io/

Launch a virtual server 
-----
::

    git clone https://github.com/pysqz/vagrant-bae.git
    cd vagrant-bae
    vagrant up

Log onto your Ubuntu server
----
::

    ### ʹ��vagrant������
    vagrant ssh

    ### ֱ��ʹ��ssh (username:root, password:vagrant)
    ssh root@127.0.0.1 -p 10022

Playing with BAE3.0
----
*��phpӦ��Ϊ��*
::

    svn co https://svn.duapp.com/${your_appid} /home/app/php-app/

    cd /home/admin/php-runtime

    ./build.sh

    ./run.sh start

    ### BAE3.0��php-webģ�⻷���Ѿ�����
    ### ʹ��curl�������Ӧ�ã����Դ���
    curl 127.0.0.1:8080

    ### ʹ��host�������������
    127.0.0.1:10080

.. _BAE3: http://developer.baidu.com/events/bae3

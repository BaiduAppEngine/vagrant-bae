VAGRANT-BAE
======================

Overview
--------
vagrant-bae��һ���������⻯��������vagrant����İ��� BAE3_ ִ�е�Ԫ����ģ���Ubuntu (12.04.2 LTS)�����������
�����ڲ����� BAE3_ ����ͬ����ִ�л��������ڿ������ڱ��ص��ԡ����д��롣

Installation
-------------
1. ��װ virtualbox https://www.virtualbox.org����ϸ���̲μ������ĵ�
2. ��װ vagrant http://www.vagrantup.com����ϸ���̲μ������ĵ����Ƽ��汾>=1.2.2
3. ��װ git http://git-scm.com/downloads ����(for windows) http://msysgit.github.io/ 


Usage
-----
Launch a virtual server 
+++++++++++++++++++++++
::

    git clone https://github.com/pysqz/vagrant-bae.git
    cd vagrant-bae
    vagrant up

Log onto your Ubuntu server
+++++++++++++++++++++++++++
::
 
    ### ʹ��vagrant�����Ĭ���û�Ϊvagrant�����鿪�����л���root����
    vagrant ssh

    ### ����ֱ��ʹ��ssh (username:root, password:vagrant)
    ssh root@127.0.0.1 -p 10022

Playing with BAE3.0
+++++++++++++++++++
���ؿ��������м�����BAE3.0�ͻ��˹��� cli_ �������߿��Խ���cli��Ӧ������б��ز��𼰵��ԡ� 

*��phpӦ��Ϊ��*
::
    ### ��������Ϣ��ʼ��
    bae login

    ### ��ȡBAEӦ�ã�����ID���ڹ������̨Ӧ��"������Ϣ"�л�ȡ
    bae app setup -I <ID> 

    ### �������붼���ػ���
    bae app publish --local

    ### ���������������ͨ�����·�ʽ����Ӧ�á������޸Ĵ��룬��������

    ### 1.�������ʹ��curl�������
    ###### php��pythonӦ�ÿ�ָ��Ӧ��������ͬʱ������Ӧ�ã���������ͨ��bae app list��ȡ
    curl 127.0.0.1:8080 -H "Host: $app_domain"
    ###### javaӦ��ֱ��ָ����Ӧ��war����(root.warֱ��ͨ��/����)
    curl 127.0.0.1:8080/$war_name/

    ### 2.��������ʹ�����������
    ###### php��python���޸�ϵͳhosts�ļ�����127.0.0.1��Ϊָ����Ӧ������
    app_domain:10080
    ###### javaӦ��ͬ��ָ����Ӧ��war����(root.warֱ��ͨ��/����)
    127.0.0.1:10080/$war_name/

    ### �����߿�ִ�жԱ��ػ������server�Ŀ���
    bae instance restart --local
    bae instance start --local
    bae instance stop --local

    ### ����cli������ϸ������ο� http://godbae.duapp.com/?p=338

Note
----
1. �򴴽�64bit����������迪���������VT���ԡ�һ�����ΪBIOS > Security > OS Security > Intel Virtualization Technology(ENABLE)
2. ȷ����Ļ�����ssh��ʹ�ã���� http://www.openssh.org/
3. ȷ����Ļ�����ϵͳ�̻��Ŀ¼��2G���У���virtualboxʹ�õ��������Ҳ�洢��ϵͳ�̻��Ŀ¼����������Ҫ4G����
4. ִ��"vagrant up"������ʾ"Waiting for VM to boot. This can take a few minutes."����ס��������ɲο�https://github.com/mitchellh/vagrant/issues/455��ǿ��������Ϊ��virtualbox���ֶ������������

.. _BAE3: http://developer.baidu.com/events/bae3
.. _cli: http://godbae.duapp.com/?p=338
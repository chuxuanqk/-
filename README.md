# -
���ú�Python3.6��pip3
��װEPEL��IUS���Դ

yum install epel-release -y
yum install https://centos7.iuscommunity.org/ius-release.rpm -y
��װPython3.6

yum install python36u -y
yum install python36u-devel -y
����python3���ӷ�

ln -s /bin/python3.6 /bin/python3
��װpip3

yum install python36u-pip -y
����pip3���ӷ�

ln -s /bin/pip3.6 /bin/pip3

��װuwsgi
python3 -m pip install uwsgi

������Ŀ����
�ڷ������ϴ�����Django��Ŀhello�����uwsgi+Django+nginx��

Ȼ��ʹ��������������uwsgi��

uwsgi �Cini uwsgi.ini
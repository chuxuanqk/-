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

��װnginx
cd ~
yum install pcre pcre-devel
yum install openssl openssl-devel
wget http://nginx.org/download/nginx-1.5.6.tar.gz
tar xf nginx-1.5.6.tar.gz
cd nginx-1.5.6
./configure --prefix=/usr/local/nginx-1.5.6 \
--with-http_stub_status_module \
--with-http_gzip_static_module
make && make install
ln -s /usr/local/nginx-1.5.6/sbin/nginx /bin/nginx 


������Ŀ����
�ڷ������ϴ�����Django��Ŀhello�����uwsgi+Django+nginx��

Ȼ��ʹ��������������uwsgi��

uwsgi �Cini uwsgi.ini

����uwsgi��
uwsgi �Cini /root/Code/Tax_consult/mysite_uwsgi.ini

����nginx��
nginx -c /root/Code/Tax_consult/mysite_nginx.conf


���°����� Nginx ���õļ������

/usr/local/webserver/nginx/sbin/nginx -s reload            # �������������ļ�
/usr/local/webserver/nginx/sbin/nginx -s reopen            # ���� Nginx
/usr/local/webserver/nginx/sbin/nginx -s stop              # ֹͣ Nginx

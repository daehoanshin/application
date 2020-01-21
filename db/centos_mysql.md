# MySQL 설치

Centos7 부터 MariaDB가 기본 DB가 되어버려서 yum으로 MySQL 설치가 불가능합니다.

그래서 별도의 MySQL repository 추가해줘야 합니다.

MySQL repository를 추가하고, mysql 설치까지 하는 과정을 진행해보겠습니다.



먼저, 아래와 같이 입력하여 rpm 파일을 받아옵니다.

[root@localhost ~]# wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm


해당 rpm 파일을 설치해야 repository에 추가됩니다.

[root@localhost ~]# rpm -ivh mysql-community-release-el7-5.noarch.rpm

yum -y install mysql-server


[root@localhost ~]# service mysqld start
Redirecting to /bin/systemctl start  mysqld.service
[root@localhost ~]# mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 2
Server version: 5.6.33 MySQL Community Server (GPL)

Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>



보다시피 현재 서버의 character set이 latin1입니다.

이 상태에선 서버에 한글 데이터를 저장하지 못합니다. utf-8로 변경해줘야겠네요.



set character_set_server=utf8

set character_set_database=utf8

로도 변경할 수 있지만.. 휘발성이라 현재 세션에서만 해당합니다. 로그아웃하고 들어오면 다시 latin1이 되죠.



영구적으로 변경하려면 MySQL의 모든 설정이 다 들어있는 my.cnf 파일을 수정해줘야 합니다. /etc 폴더에 있습니다.

vi 편집기로 들어가신 뒤~ 아래와 같이 작성해주시면 됩니다.

[client]
default-character-set=utf8

[mysql]
default-character-set=utf8

[mysqld]

datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock

character-set-server=utf8
collation-server=utf8_general_ci
init_connect=SET collation_connection = utf8_general_ci
init_connect=SET NAMES utf8

character-set-client-handshake = FALSE
skip-character-set-client-handshake

[mysqldump]
default-character-set=utf8


# MySQL root 비밀번호 설정
mysqladmin -u root -p password '새로운비밀번호'
mysqladmin -u root -p password 'bitek01!'

2. update문을 이용하여 root 비밀번호 설정



mysql>show databases;                                             //데이터베이스 목록 확인

mysql>use mysql;                                                    //mysql 데이터베이스 사용

mysql>update user set password=password('새로운비밀번호') where user='root';       //root의 비밀번호를 설정

mysql>flush privileges;                                             //변경된 설정 적용


# 외부접속

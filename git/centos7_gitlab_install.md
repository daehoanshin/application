# 안됨
[wiki](https://wikidocs.net/16279)
```
$ sudo yum install curl policycoreutils openssh-server openssh-clients
$ sudo systemctl enable sshd
$ sudo systemctl start sshd
$ sudo yum install postfix
$ sudo systemctl enable postfix
$ sudo systemctl start postfix


curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash
yum install gitlab-ce
```

* smtp 설정

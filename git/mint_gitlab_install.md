# 안됨
```
sudo apt-get update
sudo apt-get install -y curl openssh-server ca-certificates
sudo apt-get install -y postfix

curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash

sudo EXTERNAL_URL="http://gitlab.sdhlab.com" apt-get install gitab-ce

```


* [youtube](https://www.youtube.com/watch?v=6FgpFqx8L-E)
* [blog](https://www.linuxhelp.com/how-to-install-gitlab-on-linuxmint-19)

* root 접속
```
lsb_release -a
apt install openssh-server postfix gdebi
gdebi gitlab-ce_12.1.0-ce.0_amd64.deb
gitlab-ctl reconfigure

```

* 재시작
```
gitlab-ctl restart
```

* smtp 설정
```
gitlab_rails['smtp_enable'] = true
gitlab_rails['smtp_address'] = "smtp.gmail.com"
gitlab_rails['smtp_port'] = 587
gitlab_rails['smtp_user_name'] = "my.email@gmail.com"
gitlab_rails['smtp_password'] = "my-gmail-password"
gitlab_rails['smtp_domain'] = "smtp.gmail.com"
gitlab_rails['smtp_authentication'] = "login"
gitlab_rails['smtp_enable_starttls_auto'] = true
gitlab_rails['smtp_tls'] = false
gitlab_rails['smtp_openssl_verify_mode'] = 'peer'
```

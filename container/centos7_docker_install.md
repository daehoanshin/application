[centos7](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-centos-7)

* Step 1 — Installing Docker
`The Docker installation package available in the official CentOS 7 repository may not be the latest version. To get the latest and greatest version, install Docker from the official Docker repository. This section shows you how to do just that.

But first, let’s update the package database:`

```
sudo yum check-update
curl -fsSL https://get.docker.com/ | sh

sudo systemctl start docker
sudo systemctl status docker

sudo systemctl enable docker
```



`Verify that it’s running:


The output should be similar to the following, showing that the service is active and running:

Output
● docker.service - Docker Application Container Engine
   Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
   Active: active (running) since Sun 2016-05-01 06:53:52 CDT; 1 weeks 3 days ago
     Docs: https://docs.docker.com
 Main PID: 749 (docker)
Lastly, make sure it starts at every server reboot:`


* Step 2 — Executing Docker Command Without Sudo
`sudo usermod -aG docker $(whoami)`

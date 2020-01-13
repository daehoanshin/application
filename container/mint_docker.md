# 다안됨
Step 1: Install Dependency packages
Start the installation by ensuring that all the packages used by docker as dependencies are installed.

sudo apt-get update
sudo apt-get -y install apt-transport-https ca-certificates curl software-properties-common

Step 2: Add Docker’s official GPG key:
Import Docker GPG key used for signing Docker packages.

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

Step 3: Add the Docker repository to Linux Mint 19
Add Docker upstream repository to your Linux Mint 19 so you can install the latest stable release of Docker.

# 안됨 sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(. /etc/os-release; echo "$UBUNTU_CODENAME") stable"

export LSB_ETC_LSB_RELEASE=/etc/upstream-release/lsb-release
V=$(lsb_release -cs)
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu ${V} stable"


The command above will add a new line to additional repositories file.

$ cat /etc/apt/sources.list.d/additional-repositories.list
deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable

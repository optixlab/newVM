# Zsh
sudo apt-get install Zsh

## oh-my-zsh
Look up curl method of downloading it. Use " | bash" instead of sh 
$ sudo chsh -s $(which zsh) $(whoami)


# Download Dropbox 
## [Ref](http://buildcontext.com/blog/2012/dropbox-linux-ubuntu-ec2-linode-selective-sync)

   * uname -m
   * cd ~
   * wget
   * wget -O - "http://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -
   * mkdir utils
   * wget -O ~/utils/dropbox.py "http://www.dropbox.com/download?dl=packages/dropbox.py"
   * chmod 755 ~/utils/dropbox.py
   * wget -O ~/utils/dropbox_temp "https://raw.github.com/gist/2347727/108fc8af551cb4fdf7cdd08b891a45f405d283dc/dropbox"

# ssh keygen add to github
## [Koding](https://koding.com/Activity/steps-clone-projects-github-koding-1-create-account-github-2-open-your-terminal-3)
## [Ref](help.github.com/articles/generating-ssh-keys)
### [Comparing Cloud IDE](http://readwrite.com/2014/08/14/cloud9-koding-nitrousio-integrated-development-environment-ide-coding)

  * ssh-keygen -t rsa -C "optixlab@gmail.com"
  * ssh-agent -s
  * ssh-add ~/.ssh/id_rsa

# Docker Installation
## [Ref](http://learn.koding.com/guides/what-is-docker/)

* sudo apt-get update
* sudo apt-get install docker.io
* sudo ln -df /usr/bin/docker.io /usr/local/bin/docker
* sudo sed -i '$acomplete -F _docker docker' /etc/bash.completion.d/docker.io
* source /etc/bash_completion.d/docker.io
* Add Docker repo key to the local keychain
  sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9

* Add Docker repo to the apt sources list, update and install lxc package
  sudo sh -c "echo deb https://get.docker.com/ubuntu docker main /etc/apt/sources.list.d/docker.list"
  sudo apt-get update
  sudo apt-get install lxc-docker

* If this fails, use the following:
  curl -sSL https://get.docker.com/ubuntu/ | sudo sh

* If this works, 
  sudo docker run -i -t ubuntu /bin/bash


# New Git
## [Ref](https://www.atlassian.com/git/)

* git init
* git init <directory>
* git init --bare <directory>


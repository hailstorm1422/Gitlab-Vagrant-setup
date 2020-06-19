# Gitlab-Vagrant-setup

### Install and setup Vagrant on your host machine.

clone this repository
```
https://github.com/hailstorm1422/Gitlab-Vagrant-setup.git
cd  Gitlab-Vagrant-setup
vagrant up 
```
By default ubuntu/bionic64 machine will gitlab instance will spun up on your private_network IP http://192.168.2.17 

To change this edit the private_network parameter to a specific desired ip and prevent collision.
```
config.vm.network "private_network", ip: "192.168.2.17"
```

To SSH in to the instance by using box-id 
```
vagrant ssh box-id 
vagrant ssh d513576
```
To know the box id use global-status command
```
use vagrant global-status
```
By default for performance the memory for the box is 8129 ~ 8 gigs.
Edit the vb.memory parameter value to your custom liking. 
```
vb.memory = "8024"
```
By default the virtualization platform is VirtualBox, you can change this to VM WARE by tweaking the vm.provider parameter :
```
config.vm.provider "virtualbox"
```




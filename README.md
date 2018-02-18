# Desire Master Node Ansible

Setting up a Desire Coin masternode using automation.

Requirments
  - Vagrant
  - VirtualBox
  - Git
  
### Installation

You will need to have Vagrant and VirtualBox installed on your machine in order for this to work.

Windows/Mac download links

Download [Vagrant](https://www.vagrantup.com/downloads.html).
Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Clone the repo

```sh
$ github clone https://github.com/constantinpr/desiremasternode-ansible.git
```

Once you've cloned the repo, the only thing that's left is to replace the variables which can be found under /provisioning/roles/desiremn/defaults/main.yml with your own ones, ie :

masternodeprivkey: your master node private key
server_ip: your server IP
user: your user
password: your password

Once the vars have been updated you just need to run the command below. You will need to be in the root of the clonned repository



```sh
$ vagrant up
```

License
----

**Free Software, Hell Yeah!**

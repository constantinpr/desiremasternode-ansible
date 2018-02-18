Vagrant.configure("2") do |config|

################### nginx webserver ###########################

    config.vm.define "desiremn" do |subconfig|
    subconfig.vm.box = "bento/ubuntu-14.04"
    subconfig.vm.hostname = "desiremn"
    config.vm.provider :virtualbox do |vb|
      vb.name = "desiremn"
    end

    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
      config.vm.network "private_network", ip: "10.0.0.135"
    end

###################Ansible provisioning ########################

    config.vm.provision :ansible do |ansible|
      #ansible.verbose = "v"
      ansible.playbook = "provisioning/playbook.yml"
      ansible.groups = {
      "desiremasternode" => ["desiremn"]
    }
    end

###############################################################

end

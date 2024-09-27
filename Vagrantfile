# Vagrantfile
Vagrant.configure("2") do |config|
#  config.vm.box = "debian/bullseye64"
  config.vm.synced_folder ".", "/vagrant", mount_options: ["dmode=755,fmode=600"]
  config.vm.box = "generic/debian12"
  config.vm.box_architecture = "amd64"

  config.vm.define "pghost01" do |machine|
    machine.vm.network "private_network", ip: "172.17.177.27"
    machine.vm.hostname = "pghost01"
  end

  config.vm.define "pghost02" do |machine|
    machine.vm.network "private_network", ip: "172.17.177.28"
    machine.vm.hostname = "pghost02"
  end
  
  config.vm.define "etcd01" do |machine|
    machine.vm.network "private_network", ip: "172.17.177.29"
#    machine.vm.network "forwarded_port", guest: 2379, host: 2379
    config.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--nicpromisc2", "allow-all"]
    end
    machine.vm.hostname = "etcd01"
	
	machine.vm.provision :ansible_local do |ansible|
      ansible.playbook       = "playbook.yml"
      ansible.verbose        = true
      ansible.install        = true
      ansible.limit          = "all"
      ansible.inventory_path = "Inventory.yml"
      
    end
  end
end

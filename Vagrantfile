Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "dev-machine"
  
    # config.vm.provision "shell", path: "install-ansible.sh"
    config.vm.provision :guest_ansible do |guest_ansible|
        guest_ansible.playbook = "main.yml"    
    end
    # config.vm.network "forwarded_port", guest: 80, host: 9000, id: "nginx"
    # config.vm.network "forwarded_port", guest: 80, host: 9000, id: "nginx", protocol: "tcp"

    config.vm.provider "virtualbox" do |v|
        v.memory = 4096
        v.cpus = 2
    end
  end
  
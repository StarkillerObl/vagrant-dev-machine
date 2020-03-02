require_relative 'vagrant-machine/vagrant-variables.rb'
include VagrantVariables

Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "dev-machine"
  
    # guest_ansible require running: vagrant plugin install vagrant-guest_ansible
    config.vm.provision :guest_ansible do |guest_ansible|
        guest_ansible.playbook = "vagrant-machine/main.yml"    
    end    
    # config.vm.network "forwarded_port", guest: 80, host: 9000, id: "sample-id", protocol: "tcp"

    config.vm.provider "virtualbox" do |v|
        v.memory = 4096
        v.cpus = 2
    end
  end
  
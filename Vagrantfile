# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.require_version ">= 2.4.1"

Vagrant.configure("2") do |config|

  config.vm.box = "oraclelinux/8"
  config.vm.box_version = "8.9.511"
  config.vm.box_url = "https://oracle.github.io/vagrant-projects/boxes/oraclelinux/8.json"

  config.vm.hostname = "vm-ansible.local"
  
  config.vm.provider "virtualbox" do |v|
    v.name = "vm-ansible"
    v.memory = 4096
    v.cpus = 4
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "Ansible/main.yml"
  end  

end

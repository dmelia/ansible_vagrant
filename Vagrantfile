# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  
  config.vm.define "slave" do |slave|
    slave.vm.box = "ubuntu/bionic64"
	slave.vm.network "private_network", ip: "192.168.56.12", use_dhcp_assigned_default_route: true
	slave.vm.synced_folder "slave/", "/vagrant"
  end
  
  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/bionic64"
	ansible.vm.network "private_network", ip: "192.168.56.11", use_dhcp_assigned_default_route: true
	ansible.vm.synced_folder "ansible/", "/vagrant"
  end
end


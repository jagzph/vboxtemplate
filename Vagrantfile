# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "controller" do |controller|
    controller.vm.box = "ubuntu/xenial64"
    controller.vm.hostname = 'controller'
    controller.vm.box_url = "ubuntu/xenial64"
	
    controller.vm.network "public_network", :adapter => 1
    controller.vm.network :private_network, ip: "10.0.0.11", :adapter => 2
    controller.vm.network :private_network, ip: "192.168.100.11", :adapter => 3


    controller.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "controller"]
    end
  end

  config.vm.define "compute" do |compute|
    compute.vm.box = "ubuntu/xenial64"
    compute.vm.hostname = 'compute'
    compute.vm.box_url = "ubuntu/xenial64"

    compute.vm.network "public_network", :adapter => 1
    compute.vm.network :private_network, ip: "10.0.0.31"
    #compute.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"
    compute.vm.network :private_network, ip: "192.168.100.31", :adapter => 3

    compute.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "compute"]
    end
  end

  config.vm.define "block1" do |block1|
    block1.vm.box = "ubuntu/xenial64"
    block1.vm.hostname = 'block1'
    block1.vm.box_url = "ubuntu/xenial64"

    block1.vm.network "public_network", :adapter => 1
    block1.vm.network :private_network, ip: "10.0.0.51"
    #block1.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"
    block1.vm.network :private_network, ip: "192.168.100.51", :adapter => 3
	
    block1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "block1"]
    end
  end
  
  config.vm.define "object1" do |object1|
    object1.vm.box = "ubuntu/xenial64"
    object1.vm.hostname = 'object1'
    object1.vm.box_url = "ubuntu/xenial64"

    object1.vm.network "public_network", :adapter => 1
    object1.vm.network :private_network, ip: "10.0.0.71"
    #object1.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"
    object1.vm.network :private_network, ip: "192.168.100.71", :adapter => 3

    object1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "object1"]
    end
  end 
  
  config.vm.define "object2" do |object2|
    object2.vm.box = "ubuntu/xenial64"
    object2.vm.hostname = 'object2'
    object2.vm.box_url = "ubuntu/xenial64"

    object2.vm.network "public_network", :adapter => 1
    object2.vm.network :private_network, ip: "10.0.0.72"
    #object2.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"
    object2.vm.network :private_network, ip: "192.168.100.72", :adapter => 3

    object2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "object2"]
    end
  end 
end

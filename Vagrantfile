# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Define the Ubuntu box image to use
  config.vm.box = "ubuntu/focal64" # Use ubuntu/focal64

  # Define the server node
  config.vm.define "server" do |server|
    server.vm.hostname = "server"
    server.vm.network "private_network", ip: "192.168.56.11"
    server.vm.provider "virtualbox" do |vb|
      vb.memory = "4096" # Ensure this is set to 4096MB
      vb.cpus = 2        # Set CPU to 2
      vb.gui = true      # Enable GUI mode
    end
    server.vm.boot_timeout = 1200 # Set boot timeout for server node
    server.vm.provision "shell", inline: ""
  end

  # Define the first node
  config.vm.define "node-0" do |node0|
    node0.vm.hostname = "node-0"
    node0.vm.network "private_network", ip: "192.168.56.12"
    node0.vm.provider "virtualbox" do |vb|
      vb.memory = "2048" # Set memory to 2GB
      vb.cpus = 2        # Set CPU to 2
      vb.gui = true      # Enable GUI mode
    end
    node0.vm.boot_timeout = 1200 # Set boot timeout for node-0
    node0.vm.provision "shell", inline: ""
  end

  # Define the second node
  config.vm.define "node-1" do |node1|
    node1.vm.hostname = "node-1"
    node1.vm.network "private_network", ip: "192.168.56.13"
    node1.vm.provider "virtualbox" do |vb|
      vb.memory = "2048" # Set memory to 2GB
      vb.cpus = 2        # Set CPU to 2
      vb.gui = true      # Enable GUI mode
    end
    node1.vm.boot_timeout = 1200 # Set boot timeout for node-1
    node1.vm.provision "shell", inline: ""
  end
end

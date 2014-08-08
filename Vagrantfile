# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version.
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  #
  # Vagrant box.
  #
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.hostname = "dev.local"

  #
  # Port mapping.
  #
  config.vm.network "forwarded_port", guest: 80, host: 8080

  #
  # Private network.
  #
  config.vm.network "private_network", ip: "10.10.0.10"

  #
  # Public network.
  #
  # config.vm.network "public_network", ip: "192.168.1.10"

  #
  # Sync folder.
  #
  # config.vm.synced_folder "../data", "/vagrant_data"

  # 
  # VM config.
  #
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  #
  # Provision with Bash.
  #
  config.vm.provision "shell", path: "script.sh"

end

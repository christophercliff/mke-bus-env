# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "hashicorp/precise64"
  config.vm.network :private_network, ip: "10.10.10.20"
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.synced_folder "./mke-bus/", "/mke-bus/", type: "nfs"

  config.vm.provision :shell, :inline => "sudo apt-get update"
  config.vm.provision :shell, :inline => "sudo apt-get install -y python-software-properties"
  config.vm.provision :shell, :inline => "sudo add-apt-repository ppa:chris-lea/node.js"
  config.vm.provision :shell, :inline => "sudo apt-get update"
  config.vm.provision :shell, :inline => "sudo apt-get install -y make"
  config.vm.provision :shell, :inline => "sudo apt-get install -y build-essential"
  config.vm.provision :shell, :inline => "sudo apt-get install -y nodejs"
  config.vm.provision :shell, :inline => "sudo apt-get install -y postgresql"
  config.vm.provision :shell, :inline => "sudo apt-get install -y postgresql-contrib"
  config.vm.provision :shell, :inline => "sudo apt-get install -y pgadmin3"
  config.vm.provision :shell, :inline => "sudo apt-get install -y libpq-dev"

end

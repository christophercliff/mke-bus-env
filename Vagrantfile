# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "hashicorp/precise64"
  config.vm.network "forwarded_port", guest: 8001, host: 8000
  config.vm.synced_folder "./mke-bus/", "/mke-bus/"

  config.vm.provision :shell, :inline => "sudo apt-get update"
  config.vm.provision :shell, :inline => "sudo apt-get install -y python-software-properties"
  config.vm.provision :shell, :inline => "sudo add-apt-repository ppa:chris-lea/node.js"
  config.vm.provision :shell, :inline => "sudo apt-get update"
  config.vm.provision :shell, :inline => "sudo apt-get install -y nodejs"
  config.vm.provision :shell, :inline => "sudo apt-get install -y postgresql"
  config.vm.provision :shell, :inline => "sudo apt-get install -y postgresql-contrib"
  config.vm.provision :shell, :inline => "sudo apt-get install -y pgadmin3"

end

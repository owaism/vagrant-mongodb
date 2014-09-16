# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Ubuntu 64-bit OS on the guest machine.
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  # Mongo DB will be available on host 27018 of the host.
  config.vm.network "forwarded_port", guest: 27017, host: 27018

  # Chef solo provisioning for installing MongoDB
  
  config.vm.provision "chef_solo" do |chef|
      chef.add_recipe "mongodb"
  end
end

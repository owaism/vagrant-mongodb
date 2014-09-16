vagrant-mongodb
================

A Vagrant box with a running MongoDB server. The resulting Vagrant VM is provisioned with MongoDB using Chef Solo.

# Pre-requisites

1. Working git installed
2. [Vagrant 1.5.4](http://www.vagrantup.com/downloads.html) or later installed
3. [VirtualBox 4.3.12](https://www.virtualbox.org/wiki/Downloads) or later installed

# Steps to have a working MongoDB Vagrant Box

* Execute the following in the terminal where you want to have the Vagrant Folder created.

   ```
   git clone --recursive https://github.com/equa-monde/vagrant-mongodb.git mongodb
   cd mongobdb
   vagrant up
   ```

   Wait up for the VM to initialize and startup.

* MongoDB server is up and running. It is connected to port 27018 on your local machine. To connect to MongoDB use the following from the host machine (mongo should be installed on the host machine):

   ```
   mongo --port 27018
   ```

   Else to access from the guest machine do the following

   '''
   vagrant ssh
   mongo 

   '''
# -*- mode: ruby -*-
# vi: set ft=ruby :
$script = <<SCRIPT

echo Updating depedencies...
sudo apt-get update
echo Fetching Go 1.2.1 ...
cd /tmp/
wget https://go.googlecode.com/files/go1.2.1.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.2.1.linux-amd64.tar.gz
echo "export PATH=$PATH:/usr/local/go/bin" >> /home/vagrant/.profile

SCRIPT

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "trusty64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.provision "shell", inline: $script
end

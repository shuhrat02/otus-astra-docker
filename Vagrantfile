# -*- mode: ruby -*-
# vi: set ft=ruby :
 
Vagrant.configure("2") do |config|

config.vm.box = "orel-vanilla-gui/2.12.29"
config.vm.box_url = "https://vault.astralinux.ru/vagrant/orel-vanilla-gui-2.12.29.json"
 
config.vm.provider "virtualbox" do |vb|
# Display the VirtualBox GUI when booting the machine
# vb.gui = true
 
vb.memory = "4000"
vb.cpus = 4
vb.customize ["modifyvm", :id, "--nested-hw-virt", "on"]
end

# config.vm.network "private_network", ip: "192.168.50.2"
# config.vm.hostname = "astralinux.test" 

config.vm.provision "shell", inline: <<-SHELL
sudo apt-get update
sudo apt-get install --no-install-recommends curl software-properties-common -y
 
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
 
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian stretch stable"
 
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
 
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo usermod -aG docker vagrant
SHELL
end

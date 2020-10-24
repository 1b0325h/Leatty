# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "1b0325h/Leatty"
  config.disksize.size = "50GB"
  config.vm.network "forwarded_port", guest: 80, host:9090
  config.vm.network "private_network", ip: "212.102.50.120"
  config.vm.synced_folder "./data", "/vagrant_data"
  config.vm.provision "shell", path: "provision.sh"
  config.vm.hostname = "Leatty"
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "4096"
    vb.name = "Leatty"
  end
end

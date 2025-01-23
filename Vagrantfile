# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
if Vagrant.has_plugin? "vagrant-vbguest"
config.vbguest.no_install = true
config.vbguest.auto_update = false
config.vbguest.no_remote = true
end
config.vm.define :maquina do |maquina|
maquina.vm.box = "bento/ubuntu-20.04"
maquina.vm.network :private_network, ip: "192.168.100.2"
maquina.vm.hostname = "maquina"
end

config.vm.boot_timeout=300
config.vm.provider "virtualbox" do |v|
    v.memory = 2048           # Allocate 2GB of RAM
    v.cpus = 2                # Allocate 2 CPUs
    #v.gui = true
  end
end
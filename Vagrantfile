# -*- mode: ruby -*-
# vi: set ft=ruby :

$update_script=<<SCRIPT
sudo apt -y install ansible
SCRIPT

Vagrant.configure("2") do |config|

  vm_distr=['ubuntu/trusty64','centos/7','arch']
  vm_url=['~/Downloads/trusty-server-cloudimg-amd64-vagrant-disk1.box','~/Downloads/CentOS-7-x86_64-Vagrant-2004_01.VirtualBox.box','~/Downloads/27d01dda-dd62-449e-8d9d-2d8dbf6851a6']

  config.vm.provider "virtualbox" do |vb|
      vb.cpus = '1'
      vb.memory = "2048"
    end

 #   manager.vm.provision "shell", :inline => $update_script
  
#   ips = ['192.168.56.21','192.168.56.31','192.168.56.41']
 #  ports = ['2222', '2223', '2224']
   (1..3).each do |i|
     config.vm.define "node-#{i}" do |node|
       node.vm.box = vm_distr[i - 1]
       node.vm.box_url = vm_url[i - 1]
   #    node.vm.network "forwarded_port", guest: 22, host: "#{ports[i - 1]}" 
#       node.vm.network :private_network, ip: "#{ips[i - 1]}"
     end
   end

end

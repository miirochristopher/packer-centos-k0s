# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
    config.vm.provision "shell", inline: "echo Olé :: Starting the Vagrant CentOS-7 Machine!"
	config.vm.box = "centos/CentOS-7"
	config.vm.box_url = "dist/centos-7-x64-virtualbox.box"
	config.vm.provider :virtualbox do |vbox|
        vbox.name = "CentOS-7"
		vbox.customize ["modifyvm", :id, "--memory", 1536]
		vbox.customize ["modifyvm", :id, "--cpus", 1]
	end
	config.vm.hostname = "centos"
	config.vm.network "forwarded_port", guest: 80, host: 8000
end 

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.box = "centos/7"
  config.vm.provision :docker
  config.vm.provision :docker_compose, run: "always", yml: "/vagrant/docker/docker-compose.yml"
  config.vm.network "forwarded_port", guest: 8080, host: 8080, host_ip: "127.0.0.1" #docker-compose, service: jenkins 		#TODO: parametrize
  config.vm.network "forwarded_port", guest: 8090, host: 8090, host_ip: "127.0.0.1" #docker-compose, service: confluence 	#TODO: parametrize
  config.vm.network "forwarded_port", guest: 8000, host: 8000, host_ip: "127.0.0.1" #docker-compose, service: jira 			#TODO: parametrize
  
  config.vm.network "forwarded_port", guest: 7990, host: 7990, host_ip: "127.0.0.1" #docker-compose, service: bitbucket	 	#TODO: parametrize 
  config.vm.network "forwarded_port", guest: 7999, host: 7999, host_ip: "127.0.0.1" #docker-compose, service: bitbucket		#TODO: parametrize
  config.vm.network "forwarded_port", guest: 8081, host: 8081, host_ip: "127.0.0.1" #docker-compose, service: artifactory	#TODO: parametrize
  config.vm.network "forwarded_port", guest: 9000, host: 9000, host_ip: "127.0.0.1" #docker-compose, service: sonarqube		#TODO: parametrize
  config.vm.network "forwarded_port", guest: 9092, host: 9092, host_ip: "127.0.0.1" #docker-compose, service: sonarqube		#TODO: parametrize
  config.vm.network "forwarded_port", guest: 5000, host: 5000, host_ip: "127.0.0.1" #docker-compose, service: registry 		#TODO: parametrize
  
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end

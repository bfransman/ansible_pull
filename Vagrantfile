# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|



  config.ssh.insert_key = false

  config.vm.define "prd-ansible-pull" do |vagrant1|
    vagrant1.vm.box = "geerlingguy/centos6"
    vagrant1.vm.hostname = "prd-ansible-pull.sciquest.com.yml"
    vagrant1.vm.network "forwarded_port", guest: 80, host: 8080
    vagrant1.vm.network "forwarded_port", guest: 443, host: 8443
  end
  config.vm.define "stg-ansible-pull" do |vagrant2|
    vagrant2.vm.box = "geerlingguy/centos6"
    vagrant2.vm.hostname = "stg-ansible-pull.sciquest.com.yml"
    vagrant2.vm.network "forwarded_port", guest: 80, host: 8081
    vagrant2.vm.network "forwarded_port", guest: 443, host: 8444
  end
  config.vm.define "dev-ansible-pull" do |vagrant3|
    vagrant3.vm.box = "geerlingguy/centos6"
    vagrant3.vm.hostname = "dev-ansible-pull.sciquest.com.yml"
    vagrant3.vm.network "forwarded_port", guest: 80, host: 8082
    vagrant3.vm.network "forwarded_port", guest: 443, host: 8445
  end

end

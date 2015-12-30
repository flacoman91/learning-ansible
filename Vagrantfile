# Defines our Vagrant environment
#
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # create webserver node
  config.vm.define :mgmt do |mgmt_config|
      mgmt_config.vm.box = "parallels/ubuntu-14.04"
      mgmt_config.vm.hostname = "mgmt"
      mgmt_config.vm.synced_folder "site/", "/var/www/shit", owner: "www-data", group: "www-data"
      mgmt_config.vm.network :private_network, ip: "10.0.15.10"
      mgmt_config.hostsupdater.aliases = ["lamp.local", "test.local"]
      mgmt_config.vm.network "forwarded_port", guest: 80, host: 8080
      mgmt_config.vm.provider "parallels" do |prl|
        prl.memory = "256"
      end
      mgmt_config.vm.provision :shell, path: "bootstrap-mgmt.sh"
  end

end

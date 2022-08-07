# -*- mode: ruby -*-
# vi: set ft=ruby :

ubuntu_version = ENV["UBUNTU_VERSION"] || "2004"

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu" + ubuntu_version
  config.vm.network "forwarded_port", guest: 19999, host: 19999, host_ip: "127.0.0.1"
  config.vm.synced_folder "./netdata_package", "/usr/local/src/netdata_package"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yaml"
  end
end

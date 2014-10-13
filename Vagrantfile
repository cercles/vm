# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "trusty64"
  config.vm.box_url = "https://vagrantcloud.com/ubuntu/trusty64/version/1/provider/virtualbox.box"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.host_key_checking = false
  end
  config.vm.provider "virtualbox" do |v|
    v.gui = true
  end
end

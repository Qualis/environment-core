# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box_url = "https://vagrantcloud.com/ubuntu/trusty64"
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
    ansible.tags = "core"
  end

  if Vagrant.has_plugin?("vagrant-cachier")
    config.cache.scope = :machine
  end
end

# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.provider :virtualbox do |v|
    v.name = "orkjern_local"
    v.memory = 512
    v.cpus = 2
  end
  config.vm.define :orkjern_local do |orkjern_local|
  end

  config.vm.provision "shell" do |s|
    s.inline = "apt-get install -y python"
  end

  # Ansible provisioner.
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
    ansible.inventory_path = "provisioning/inventory"
    ansible.verbose = "v"
    ansible.sudo = true
  end

end

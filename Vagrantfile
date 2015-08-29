# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
    config.vm.provider "libvirt" do |libvirt|
        libvirt.driver = "kvm"
        libvirt.memory = 2048
        libvirt.cpus = 2
        libvirt.storage :file, :size => '20G'
    end
 config.vm.provision :ansible do |ansible|
     ansible.playbook = "provisioning/singlenode.yml"
 end
end

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.boot_timeout = 900
  config.vm.define "unac-sv-master" do |unac|
    unac.vm.box = "bento/debian-12"
    unac.vm.network "private_network", ip: "192.168.50.11"
    unac.vm.network "forwarded_port", guest: 22, host: 2222, id: "ssh", auto_correct: true
    unac.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "2"
    end
    unac.vm.disk :disk, size: "10GB", primary: true
  end

  config.vm.define "unac-sv-1" do |unac|
    unac.vm.box = "bento/debian-12"
    unac.vm.network "private_network", ip: "192.168.50.12"
    unac.vm.network "forwarded_port", guest: 22, host: 2223, id: "ssh", auto_correct: true
    unac.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "2"
    end
    unac.vm.disk :disk, size: "10GB", primary: true
  end

  config.vm.define "unac-sv-2" do |unac|
    unac.vm.box = "bento/debian-12"
    unac.vm.network "private_network", ip: "192.168.50.13"
    unac.vm.network "forwarded_port", guest: 22, host: 2224, id: "ssh", auto_correct: true
    unac.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "2"
    end
    unac.vm.disk :disk, size: "10GB", primary: true
  end
end

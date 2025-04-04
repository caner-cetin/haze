# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.boot_timeout = 900
  config.vm.define "UNAC" do |unac|
    unac.vm.box = "bento/debian-12"
    unac.vm.box_check_update = false
    unac.vm.network "private_network", ip: "192.168.50.11"
    unac.vm.network "forwarded_port", guest: 22, host: 2222, id: "ssh", auto_correct: true
    unac.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "512"
      v.vmx["numvcpus"] = "1"
    end
    unac.vm.disk :disk, size: "10GB", primary: true
  end

  config.vm.define "UNAC-SV" do |unac_sv|
    unac_sv.vm.box = "bento/ubuntu-22.04"
    unac_sv.vm.box_check_update = false
    unac_sv.vm.network "private_network", ip: "192.168.50.12"
    unac_sv.vm.network "forwarded_port", guest: 22, host: 2223, id: "ssh", auto_correct: true

    unac_sv.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "1"
    end
  end

  config.vm.define "UNAC-W1" do |unac_w1|
    unac_w1.vm.box = "bento/ubuntu-22.04"
    unac_w1.vm.box_check_update = false
    unac_w1.vm.network "private_network", ip: "192.168.50.13"
    unac_w1.vm.network "forwarded_port", guest: 22, host: 2224, id: "ssh", auto_correct: true

    unac_w1.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "1"
    end
  end

  config.vm.define "UNAC-W2" do |unac_w2|
    unac_w2.vm.box = "bento/ubuntu-22.04"
    unac_w2.vm.box_check_update = false
    unac_w2.vm.network "private_network", ip: "192.168.50.14"
    unac_w2.vm.network "forwarded_port", guest: 22, host: 2225, id: "ssh", auto_correct: true

    unac_w2.vm.provider "vmware_desktop" do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "1"
    end
  end
end

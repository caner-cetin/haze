# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.boot_timeout = 900
  config.vm.define "IBIS" do |ibis|
    ibis.vm.box = "bento/debian-12"
    ibis.vm.network "forwarded_port", guest: 22, host: 2222, id: "ssh", auto_correct: true
    ibis.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpus", "1", "--memory", "512"]
    end
    ibis.vm.disk :disk, size: "10GB", primary: true
  end
  config.vm.define "IB-SV" do |ib_sv|
    ib_sv.vm.box = "bento/ubuntu-22.04"
    ib_sv.vm.network "forwarded_port", guest: 22, host: 2223, id: "ssh", auto_correct: true
    ib_sv.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpus", "1", "--memory", "2048"]
    end
    ib_sv.vm.disk :disk, size: "20GB", primary: true
  end
  config.vm.define "IB-W1" do |ib_w1|
    ib_w1.vm.box = "bento/ubuntu-22.04"
    ib_w1.vm.network "forwarded_port", guest: 22, host: 2224, id: "ssh", auto_correct: true
    ib_w1.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpus", "1", "--memory", "2048"]
    end
    ib_w1.vm.disk :disk, size: "20GB", primary: true
  end
  config.vm.define "IB-W2" do |ib_w2|
    ib_w2.vm.box = "bento/ubuntu-22.04"
    ib_w2.vm.network "forwarded_port", guest: 22, host: 2225, id: "ssh", auto_correct: true
    ib_w2.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpus", "1", "--memory", "2048"]
    end
    ib_w2.vm.disk :disk, size: "20GB", primary: true
  end
end

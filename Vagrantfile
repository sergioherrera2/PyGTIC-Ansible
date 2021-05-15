# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/trusty64"

  
  config.vm.define "node1" do |node1|
    node1.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
    node1.vm.hostname = "BrokerMQTT"
    node1.vm.network "public_network", bridge: "wlp2s0"
    node1.vm.provider "virtualbox" do |vb|
     vb.memory = "1024"
     vb.cpus = "1"
    end
  end
  
  config.vm.define "node2" do |node2|
    node2.vm.network "forwarded_port", guest: 80, host: 8081, host_ip: "127.0.0.1"
    node2.vm.hostname = "Telegraf"
    node2.vm.network "public_network", bridge: "wlp2s0"
    node2.vm.provider "virtualbox" do |vb|
     vb.memory = "512"
     vb.cpus = "1"
    end
  end
  
  config.vm.define "node3" do |node3|
    node3.vm.network "forwarded_port", guest: 80, host: 8082, host_ip: "127.0.0.1"
    node3.vm.hostname = "InfluxDB"
    node3.vm.network "public_network", bridge: "wlp2s0"
    node3.vm.provider "virtualbox" do |vb|
     vb.memory = "512"
     vb.cpus = "1"
    end
  end

  config.vm.define "node4" do |node4|
    node4.vm.network "forwarded_port", guest: 80, host: 8083, host_ip: "127.0.0.1"
    node4.vm.hostname = "Grafana"
    node4.vm.network "public_network", bridge: "wlp2s0"
    node4.vm.provider "virtualbox" do |vb|
     vb.memory = "512"
     vb.cpus = "1"
    end
  end
  
end

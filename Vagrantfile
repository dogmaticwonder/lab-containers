Vagrant.configure("2") do |config|

  config.vm.define "d-master" do |cfg|
    cfg.vm.box = "ubuntu/bionic64"    
    cfg.vm.box_check_update = false
    cfg.vm.hostname = "d-master"
    cfg.vm.communicator = "ssh"
    # cfg.vm.network :public_network, ip: "10.100.50.2", dns: "8.8.8.8", bridge: "en1: Wi-Fi (AirPort)"
    cfg.vm.network :private_network, ip: "10.100.50.2", dns: "8.8.8.8"

    cfg.vm.provider "virtualbox" do |vb, override|
      vb.gui = false
      vb.name = "d-master"
      vb.memory = 1024
      vb.cpus = 1
      # vb.default_nic_type = "82545EM"
      vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["setextradata", "global", "GUI/SuppressMessages", "all" ]
    end
  end

    config.vm.define "d-node1" do |cfg|
    cfg.vm.box = "ubuntu/bionic64"    
    cfg.vm.box_check_update = false
    cfg.vm.hostname = "d-node1"
    cfg.vm.communicator = "ssh"
    cfg.vm.network :private_network, ip: "10.100.50.3", dns: "8.8.8.8"
    cfg.vm.provider "virtualbox" do |vb, override|
      vb.gui = false
      vb.name = "d-node1"
      vb.memory = 1024
      vb.cpus = 1
      # vb.default_nic_type = "82545EM"
      vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["setextradata", "global", "GUI/SuppressMessages", "all" ]
    end
  end

    config.vm.define "d-node2" do |cfg|
    cfg.vm.box = "ubuntu/bionic64"    
    cfg.vm.box_check_update = false
    cfg.vm.hostname = "d-node2"
    cfg.vm.communicator = "ssh"
    cfg.vm.network :private_network, ip: "10.100.50.4", dns: "8.8.8.8"
    cfg.vm.provider "virtualbox" do |vb, override|
      vb.gui = false
      vb.name = "d-node2"
      vb.memory = 1024
      vb.cpus = 1
      # vb.default_nic_type = "82545EM"
      vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      vb.customize ["setextradata", "global", "GUI/SuppressMessages", "all" ]
    end
  end
end

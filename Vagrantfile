Vagrant.configure("2") do |config|
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.box = "debian/buster64"
  config.vm.box_check_update = false

  config.vm.define "host1" do |host|
  host.vm.hostname = "host1"
  host.vm.network "private_network", ip: "10.0.0.111"
  host.vm.provision "shell", inline:sudo apt update && sudo apt-get install ansible -y
  host.vm.provider "virtualbox" do |vb|
    vb.name = "host1"
    vb.memory = "512"
    vb.cpus = 1
  end

  config.vm.define "host2" do |host|
  host.vm.hostname = "host2"
  host.vm.network "private_network", ip: "10.0.0.112"
  host.vm.provision "shell", inline:sudo apt update && sudo apt-get install ansible -y
  host.vm.provider "virtualbox" do |vb|
    vb.name = "host2"
    vb.memory = "512"
    vb.cpus = 1
  end

  config.vm.define "host3" do |host|
  host.vm.box = "centos/7"
  host.vm.hostname = "host3"
  host.vm.network "private_network", ip: "10.0.0.110"
  host.vm.provision "shell", inline:yum update && yum install ansible -y
  host.vm.provider "virtualbox" do |vb|
      vb.name = "host3"
      vb.memory = "512"
      vb.cpus = 1
  end
end


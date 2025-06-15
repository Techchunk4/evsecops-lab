Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  nodes = {
    "monitoring-vm" => "192.168.56.10",
    "lamp-vm"       => "192.168.56.11",
    "java-app-vm"   => "192.168.56.12",
    "ci-cd-vm"      => "192.168.56.13"
  }

  nodes.each do |name, ip|
    config.vm.define name do |node|
      node.vm.hostname = name
      node.vm.network "private_network", ip: ip
      node.vm.provider "virtualbox" do |vb|
        vb.memory = 2048
        vb.cpus = 1
      end
      node.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y python3 python3-pip
      SHELL
    end
  end
end

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  nodes = {
    "monitoring-vm" => "your-ip",
    "lamp-vm"       => "our-ip"",
    "java-app-vm"   => "our-ip"",
    "ci-cd-vm"      => "our-ip""
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

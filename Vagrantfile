Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  config.vm.network "forwarded_port", guest: 2222, host: 22
  config.vm.network "forwarded_port", guest: 25565, host: 25565

  config.vm.network "public_network", bridge: "en0: Wi-Fi (AirPort)"

  config.vm.provider "virtualbox" do |vb|
     vb.cpus = 2
     vb.memory = 2048
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "minecraft-server.yml"
  end
end

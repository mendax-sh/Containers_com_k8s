Vagrant.configure("2") do |config|
    config.vm.box = "debian/bullseye64"
    config.vm.network "public_network"
  
    config.vm.provider "virtualbox" do |v|
        v.gui = false
        v.memory = "2048"
    end
  
     config.vm.provision "shell", path: "install.sh"
  end
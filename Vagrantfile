# -*- mode: ruby -*-
# vi: set ft=ruby :

vms = {
  'master' => {'memory' => '2048', 'cpus' => 2, 'ip' => '10'}
}

Vagrant.configure('2') do |config|

  config.vm.box = 'debian/buster64'
  config.vm.box_check_update = false
  
  vms.each do |name, conf|
    config.vm.define "#{name}" do |k|
      k.vm.hostname = "#{name}.cadmus"
      k.vm.network 'private_network', ip: "172.27.11.#{conf['ip']}"
      k.vm.provider 'virtualbox' do |vb|
        vb.memory = conf['memory']
        vb.cpus = conf['cpus']
      end
    end
  config.vm.provision "shell", path: "instala_geral.sh"
  end
end
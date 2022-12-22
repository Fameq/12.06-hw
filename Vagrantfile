Vagrant.configure("2") do |config|
config.vm.define "master" do |master|
  master.vm.box = "ubuntu"
  master.vm.hostname = "master-node"
  master.vm.network "public_network", ip: "192.168.5.100"
  master.vm.provider "virtualbox" do |vb|
      vb.memory = 4096
      vb.cpus = 2
  end
end
(1..1).each do |i|
config.vm.define "node0#{i}" do |node|
node.vm.box = "ubuntu"
node.vm.hostname = "worker-node0#{i}"
node.vm.network "public_network", ip: "192.168.5.10#{i}"
node.vm.provider "virtualbox" do |vb|
vb.memory = 4096
vb.cpus = 2
end
end
end
end

CHANGE MASTER TO MASTER_HOST = '192.168.5.100', MASTER_USER = 'slave', MASTER_PASSWORD = '123456789', MASTER_LOG_FILE = 'binlog.000001' , MASTER_LOG_POS = 157;


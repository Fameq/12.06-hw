Vagrant.configure("2") do |config|
config.vm.define "master" do |master|
  master.vm.box = "generic/ubuntu2204"
  master.vm.hostname = "master-node"
  master.vm.network "public_network", ip: "192.168.5.100"
  master.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
  end
end
(1..1).each do |i|
config.vm.define "node0#{i}" do |node|
node.vm.box = "generic/ubuntu2204"
node.vm.hostname = "worker-node0#{i}"
node.vm.network "public_network", ip: "192.168.5.10#{i}"
node.vm.provider "virtualbox" do |vb|
vb.memory = 1024
vb.cpus = 1
end
end
end
end
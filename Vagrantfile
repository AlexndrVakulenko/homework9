Vagrant.configure(2) do |config|
  config.vm.box = "almalinux/9"

 config.vm.provider "virtualbox" do |v|
   v.memory = 2048
   v.cpus = 1
 end

 config.vm.define "almatest" do |almatest|
   almatest.vm.network "private_network", ip: "192.168.50.10", virtualbox__intnet: "net1"
   almatest.vm.network "public_network", type: "dhcp"
   almatest.vm.synced_folder "vmshare/", "/vagrant"
   almatest.vm.hostname = "almatest"

 end


end

Vagrant.configure("2") do |config|


  config.vm.define "master" do |subconfig|
    subconfig.vm.box = "bento/ubuntu-22.04"
    subconfig.vm.hostname= "master"
    subconfig.vm.provider "master" do |v|
      v.customize ["modifyvm" , :id, "--cpuexecutioncap", "30"]
    end
    subconfig.vm.network:private_network, ip: "172.30.1.20"
  end

  config.vm.define "worker1" do |subconfig|
    subconfig.vm.box = "bento/ubuntu-22.04"
    subconfig.vm.hostname= "worker1"
    subconfig.vm.provider "worker1" do |v|
      v.customize ["modifyvm" , :id, "--cpuexecutioncap", "30"]
    end
    subconfig.vm.network:private_network, ip: "172.30.1.21"
  end

  config.vm.define "worker2" do |subconfig|
    subconfig.vm.box = "bento/ubuntu-22.04"
    subconfig.vm.hostname= "worker2"
    subconfig.vm.provider "worker2" do |v|
      v.customize ["modifyvm" , :id, "--cpuexecutioncap", "30"]
    end
    subconfig.vm.network:private_network, ip: "172.30.1.22"
  end

end

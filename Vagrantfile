Vagrant.configure("2") do |config|
    config.vm.provision "shell", inline: "echo Config docker swarm cluster"
    config.vm.define "manager" do |manager|
        manager.vm.box = "bento/ubuntu-22.04"
        manager.vm.hostname = "manager"
        manager.vm.provision "shell", path: "provision.sh"
        manager.vm.network "private_network", ip: "192.168.56.2"
        manager.vm.network "forwarded_port", guest: 80, host: 8090
    end

    config.vm.define "worker1" do |worker1|
        worker1.vm.box = "bento/ubuntu-22.04"
        worker1.vm.hostname = "worker1"
        worker1.vm.provision "shell", path: "provision.sh"
        worker1.vm.network "private_network", ip: "192.168.56.3"
    end

    config.vm.define "worker2" do |worker2|
        worker2.vm.box = "bento/ubuntu-22.04"
        worker2.vm.hostname = "worker2"
        worker2.vm.provision "shell", path: "provision.sh"
        worker2.vm.network "private_network", ip: "192.168.56.4"
    end
end
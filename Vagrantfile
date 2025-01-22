Vagrant.configure("2") do |config|

  config.vm.define "soufe1" do |soufe1|
    soufe1.vm.box = "almalinux/9"
    soufe1.vm.box_version = "9.5.20241203"
    soufe1.vm.network "private_network", ip: "192.168.0.3"
    soufe1.vm.hostname = "soufe1"

  end

  config.vm.define "soube2" do |soube2|
    soube2.vm.box = "almalinux/9"
    soube2.vm.box_version = "9.5.20241203"
    soube2.vm.network "private_network", ip: "192.168.0.2"
    soube2.vm.hostname = "soube2"

    config.vm.provision :ansible do |ansible|
      ansible.limit = "all"
      ansible.playbook = "install.yaml"
    end
  end

end

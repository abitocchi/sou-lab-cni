Vagrant.configure("2") do |config|
  config.vm.define "soufe1" do |soufe1|
    soufe1.vm.box = "almalinux/9"
    soufe1.vm.box_version = "9.5.20241203"
    soufe1.vm.network "private_network", ip: "192.168.0.3"

    soufe1.dns.tld = "lab.local"
    soufe1.vm.hostname = "lab.local"
    soufe1.dns.patterns = [/^(\w+\.)soufe1.lab.local$/, /^soufe1.lab.local$/]

    soufe1.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "install.yaml"
    end

  end

  config.vm.define "soube2" do |soube2|
    soube2.vm.box = "almalinux/9"
    soube2.vm.box_version = "9.5.20241203"
    soube2.vm.network "private_network", ip: "192.168.0.2"

    soube2.dns.tld = "lab.local"
    soube2.vm.hostname = "lab.local"
    soube2.dns.patterns = [/^(\w+\.)soube2.lab.local$/, /^soube2.lab.local$/]

    soube2.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "install.yaml"
    end

  end
end

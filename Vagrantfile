Vagrant.configure("2") do |config|

  config.vm.box = "almalinux/9"
  config.vm.box_version = "9.5.20241203"

  boxes = [
      { :name => "soufe1", :ip => "192.168.0.3" },
      { :name => "soube2", :ip => "192.168.0.2" }
  ]

  boxes.each do |opts|
    config.vm.define opts[:name] do |config|

      config.vm.hostname = opts[:name]
      config.vm.network :private_network, ip: opts[:ip]

      if opts[:name] == "soube2"
        config.vm.provision "ansible" do |ansible|
          ansible.limit = "all"
          ansible.playbook = "install.yaml"
        end
      end

    end
  end

end

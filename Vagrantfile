Vagrant.configure("2") do |config|

  config.vm.define "nginx" do |server|
      server.vm.hostname = "nginx.example.com"
      server.vm.box = "fedora/38-cloud-base"
      server.vm.provider :libvirt do |libvirt|
        libvirt.cpus = 2
        libvirt.memory = 14000
      end
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end

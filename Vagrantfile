Vagrant.configure("2") do |config|

  (1..3).each do |i|
    config.vm.define "nginx-#{i}" do |server|
        server.vm.hostname = "nginx-#{i}.example.com"
        server.vm.box = "fedora/38-cloud-base"
        server.vm.provider :libvirt do |libvirt|
          libvirt.cpus = 1
          libvirt.memory = 3000
        end
    end
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end

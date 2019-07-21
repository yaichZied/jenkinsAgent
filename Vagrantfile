Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  config.vm.define "agent"
  config.vm.network "public_network", ip: "192.168.0.200"
  config.ssh.forward_agent = true
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.limit = "all"
    ansible.verbose = "vvvv"
  end

end

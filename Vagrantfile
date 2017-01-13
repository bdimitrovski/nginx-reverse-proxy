Vagrant.configure(2) do |config|
  config.vm.box = "parallels/debian-8.1"

  config.vm.network "private_network", ip: "192.168.50.10"
  config.vm.hostname = "nginx-reverse.proxy"

  config.ssh.forward_agent = true 

  config.vm.provider "parallels" do |pr| 
  	pr.memory = 2048
  end

  config.vm.provision "ansible" do |ansible|
  	ansible.playbook = "playbook-nginx-reverse-proxy.yml"
  	ansible.extra_vars = {
      ansible_ssh_user: 'vagrant'
    }
  	  ansible.groups = {
        "nginx-reverse-proxy" => ["default"]
    }
  end
end

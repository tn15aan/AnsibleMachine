Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64" # Methods for properties etc
  config.vm.network "private_network", ip: "192.168.10.100"
  config.hostsupdater.aliases = ["development.local"]

  # Run Ansible from the Vagrant Host
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end

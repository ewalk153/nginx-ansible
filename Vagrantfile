VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # config.vm.box = "hashicorp/precise64"
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "ansible" do |ansible|
    # ansible.verbose = "v"
    ansible.playbook = "nginx.yml"
  end

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 443, host: 443
end

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "private_network", ip: "-ip-please-"
  config.vm.provider "virtualbox"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "install_SES_postfix_srv.yml"
    ansible.verbose = "vvv"
    ansible.extra_vars = {
      "deployment_path" => "/vagrant/source/{{ hostname }}"
    }
  end
end


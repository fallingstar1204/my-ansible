Vagrant.configure(2) do |config|
  config.vm.box = "jaxmetalmax/debian-jessie-8.4-x32"
  config.vm.define "vagrant-server"
  config.vm.network "forwarded_port", guest: 80, host: 8000
  config.vm.network "forwarded_port", guest: 8080, host: 8082

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook/index.yml"
  end
end

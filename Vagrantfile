Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.synced_folder "salt/roots", "/srv"
  config.vm.network :forwarded_port, guest: 8000, host: 8000

  config.vm.provision :salt do |salt|
    salt.minion_config = "salt/minion"
    #salt.run_highstate = true
  end
end

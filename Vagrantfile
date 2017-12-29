Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"

  config.vm.network "private_network", ip: "192.168.50.150"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "2048"
  end

  config.vm.synced_folder ".", "/var/www",
    :owner => "www-data",
    :group => "www-data",
    :mount_options => ["dmode=777", "fmode=666"]

  config.vm.provision "ansible" do |ansible|
    ansible.galaxy_role_file = "provision/roles.yml"
    ansible.playbook = "provision/playbook.yml"
  end
end

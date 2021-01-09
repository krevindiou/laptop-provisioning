VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "krevindiou/manjaro-xfce-20.2"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "laptop-provisioning"
    vb.memory = 4096
    vb.cpus = 4
    vb.gui = true
  end
  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
    ansible.limit = "all,localhost"
    ansible.compatibility_mode = "2.0"
    ansible.install = true
  end
end

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  # https://www.vagrantup.com/docs/provisioning/ansible_common.html#galaxy_role_file
  config.vm.provision "ansible_local" do |ansible|
    ansible.galaxy_role_file = 'requirements.yml'
    ansible.playbook = "playbook.yml"
  end

  config.vm.provider 'virtualbox' do |v|
    v.memory = 1024
    v.cpus = 2
  end
end

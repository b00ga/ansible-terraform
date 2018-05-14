Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.4"

  config.vm.provision "shell", inline: 'sudo yum install -y unzip'
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "terraform.yml"
    ansible.compatibility_mode = "2.0"
  end
end

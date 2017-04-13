Vagrant.configure(2) do |config|
  config.vm.define "localhost" do |box|
    # Recommended Ubuntu 16.04 Vagrant box
    box.vm.box = "bento/ubuntu-16.04"

    # Forward agent
    box.ssh.forward_agent = "True"

    # Run Ansible playbook
    box.vm.provision "ansible_local" do |ansible|
      # Which playbook to use
      ansible.playbook = "bootstrap.yml"
    end
  end
end

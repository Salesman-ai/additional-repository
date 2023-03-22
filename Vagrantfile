Vagrant.configure("2") do |config|
    config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 2
    end
      config.vm.define "ubuntu" do |ubuntu|
      ubuntu.vm.box = "generic/ubuntu2004"
    end
    ssh_pub_key = File.readlines("/home/<username>/.ssh/id_rsa.pub").first.strip
    config.vm.provision 'shell', inline: 'mkdir -p /root/.ssh'
    config.vm.provision 'shell', inline: "echo #{ssh_pub_key} >> /root/.ssh/authorized_keys"
    config.vm.provision 'shell', inline: "echo #{ssh_pub_key} >> /home/vagrant/.ssh/authorized_keys", pr>
    config.vm.network "private_network", ip: "<ipaddress>"
  end
  
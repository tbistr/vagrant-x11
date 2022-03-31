Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian10"

  # VM間通信の設定
  # config.vm.network "private_network", ip: "固定のIP", virtualbox__intnet: "mynetwork"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = "4"
  end

  # X11の設定
  config.ssh.forward_x11 = true
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    # apt-get upgrade
    apt-get -y install x11-apps
    # something to install with apt
  SHELL
  config.vm.provision "shell", privileged: false, inline: <<-SHELL
    echo "export DISPLAY=10.0.2.2:0" >> ~/.bash_profile
  SHELL

end

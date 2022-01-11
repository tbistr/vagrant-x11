Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"

  config.ssh.forward_x11 = true

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get upgrade
    apt-get -y install x11-apps
    # something to install with apt
  SHELL

  config.vm.provision "shell", privileged: false, inline: <<-SHELL
    echo "export DISPLAY=10.0.2.2:0" >> ~/.bash_profile
  SHELL
end

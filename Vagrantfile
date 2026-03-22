# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.boot_timeout = 600

  config.vm.network "forwarded_port", guest: 8080, host: 8080

  config.vm.provision "shell", inline: <<-SHELL
    set -e

    sudo apt-get update -y
    sudo apt-get upgrade -y

    sudo locale-gen en_GB.UTF-8

    sudo apt-get install -y python3 python3-pip python3-venv python3-dev sqlite3

    python3 -m pip install --upgrade pip
  SHELL

end

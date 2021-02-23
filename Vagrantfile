Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.box_version = "20210208.0.0"
  # config.vm.box_url = "https://vagrantcloud.com/hashicorp/bionic64"
  config.vm.box_url = "https://vagrantcloud.com/ubuntu/bionic64"

  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip:"127.0.0.1"
  config.vm.network "forwarded_port", guest: 80, host: 1234, host_ip:"127.0.0.1"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider "virtualbox" do |v|
  v.gui = true
  v.memory = 1024
  v.cpus = 1
  v.customize ["modifyvm", :id, "--vram", "128"]
  end

  config.vm.provision "shell", inline: <<-SHELL
  apt-get update
  apt-get install -y vim
  SHELL

  config.vm.provision "shell", inline: <<-SHELL
  apt-get update
  apt-get install -y ansible
  SHELL

  config.vm.provision "shell", inline: <<-SHELL
  # Ajout du dépôt dans le script SHELL:
  # Ajout de la clé
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add
  # Ajout du dépot
  apt-add-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
  apt-get update
  # Install de docker et de quelques dépendances
  apt-get install -y apt-transport-https ca-certificates curl gnupg-agent docker-ce docker-ce-cli containerd.io
  # Ajout du groupe docker au user vagrant
  usermod -aG docker vagrant
  SHELL
  end
  
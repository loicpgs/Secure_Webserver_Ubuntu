Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"

  # Redirection des ports HTTP et HTTPS
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 443, host: 8443

  # Réseau privé avec IP statique (évite le DHCP)
  config.vm.network "private_network", ip: "192.168.56.10"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "secure-webserver"
    vb.memory = "1024"
    vb.cpus = 1
  end
end

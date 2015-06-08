# -*- mode: ruby -*-
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu-14.04"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provision :shell, :inline => <<-EOH
    apt-get update
    apt-get install libsqlite3-dev
    apt-get install docker.io
    wget downloads.drone.io/master/drone.deb
    dpkg --install drone.deb
    cp /vagrant/drone.toml /etc/drone/drone.toml
    sudo restart drone
  EOH

end

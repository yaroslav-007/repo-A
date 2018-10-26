Vagrant.configure("2") do |config|
  config.vm.box = "vatman/xenial64-clean"
  config.vm.box_version = "0.1"
  config.vm.hostname = "bananas3"
  config.vm.provision :shell, :path => "./scripts/install-nginx.sh", :privileged => true
  config.vm.network "private_network", ip: "192.168.56.56"
  config.vm.network "forwarded_port", guest: 80, host: 8080
end
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  # config.vm.disk :disk, size: "100GB", primary: true

  # Reserving 5 static IP addresses for the Magma Orc8r
  config.vm.network "public_network", bridge: "wlp0s20f3", ip: "192.168.0.91"
  config.vm.network "public_network", bridge: "wlp0s20f3", ip: "192.168.0.92"
  config.vm.network "public_network", bridge: "wlp0s20f3", ip: "192.168.0.93"
  config.vm.network "public_network", bridge: "wlp0s20f3", ip: "192.168.0.94"
  config.vm.network "public_network", bridge: "wlp0s20f3", ip: "192.168.0.95"

end

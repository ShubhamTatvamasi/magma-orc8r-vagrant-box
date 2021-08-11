Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.network "public_network", bridge: "ens1f0", ip: "192.168.5.51"
  config.vm.network "public_network", bridge: "ens1f0", ip: "192.168.5.52"
  config.vm.network "public_network", bridge: "ens1f0", ip: "192.168.5.53"
  config.vm.network "public_network", bridge: "ens1f0", ip: "192.168.5.54"
  config.vm.network "public_network", bridge: "ens1f0", ip: "192.168.5.55"
  config.vm.disk :disk, size: "100GB", primary: true

  config.vm.provider "virtualbox" do |v|
    v.linked_clone = true
    v.memory = 32768
    v.cpus = 8
  end

  config.vm.box_check_update = false

  config.vm.provision "shell", inline: <<-SHELL
    echo "@reboot ip route add default via 192.168.5.1" \
      > /var/spool/cron/crontabs/root
  SHELL

  config.vm.provision "shell", run: "always",
    inline: "ip route add default via 192.168.5.1 || true"

end

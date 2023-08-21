Vagrant.configure("2") do | config |
    config.vm.box = "spox/ubuntu-arm"
    # macOS kullanmayanlar için:
    # config.vm.box = "bento/ubuntu-22.04"
    # box_version satırı da silinmeli
    config.vm.box_version = "1.0.0"
    config.vm.network "private_network", ip: "192.168.56.10"
    config.vm.provider "vmware_desktop" do |vm|
        vm.gui = false
        vm.memory="2000"
        vm.allowlist_verified = true
        vm.cpus="2"
    end
end
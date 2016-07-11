# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "azureservicefabric/linuxonebox_0.3.0.1"
  config.vm.box_url = "https://servicefabricsdkpreview.blob.core.windows.net/linux/sflinuxonebox-20160708.box"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # eg. You can connect to Service Fabric Explorer at http://192.168.50.50:19080/Explorer.
  config.vm.network "private_network", ip: "192.168.50.50"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Service Fabric onebox environments require at least 2GB of memory to run
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  # Set up the onebox cluster on the VM
  config.vm.provision "shell", inline:
    "sudo bash /opt/microsoft/sdk/servicefabric/clustersetup/devclustersetup.sh"
end

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # For a complete reference, please see the online documentation at
  # vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  # The box name and SHA should be updated if the box itself changes.
  config.vm.box = 'vagrant-heroku-2580899813'
  config.vm.box_url = 'https://helpful-assets.s3.amazonaws.com/vagrant-boxes/vagrant-heroku-2580899813.box'
  config.vm.provision :shell, path: 'config/vagrant/bootstrap.sh'

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:5000" will access port 5000 on the guest machine.
  config.vm.network :forwarded_port, guest: 3000, host: 3000
end

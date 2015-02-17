# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
$script = <<SCRIPT
usermod -a -G www-data vagrant
apt-get update
apt-get install git node npm
npm install -g grunt-cli bower
gem install sass
SCRIPT

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "mayppong.github.io"
  config.vm.provision "shell", inline: $script
end

# -- mode: ruby --
# vi: set ft=ruby :
require 'yaml'
yaml = YAML.load_file("core/machines.yml")

Vagrant.configure("2") do |config|
  yaml.each do |server|
    config.vm.define server["name"] do |srv|
      srv.vm.box = server["sistema"]
      srv.vm.network "private_network", ip: server["ip"]
      srv.vm.hostname = server["hostname"]
      srv.vm.provider "virtualbox" do |vb|
        vb.name = server["name"]
        vb.memory = server["memory"]
        vb.cpus = server["cpus"]
      end
  end
end

config.vm.provision "shell", inline: <<-SHELL

if [ $HOSTNAME = "devops-lab" ]; then
  sudo apt update -y && sudo apt upgrade -y
  curl -fsSL https://get.docker.com -o get-docker.sh
  sudo sh get-docker.sh
fi;
  date +"%H:%M:%S"
  sleep 5
  date +"%H:%M:%S"
  usermod -a -G docker vagrant
SHELL

end

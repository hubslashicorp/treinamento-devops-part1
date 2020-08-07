# -- mode: ruby --
# vi: set ft=ruby :
require 'yaml'
yaml = YAML.load_file("core/machines.yml")

K8S_VERSION="1.11.7-00" 
DOCKER_VERSION="17.12.1~ce-0~ubuntu"
MYSQL_PASSWORD='devops@slashicorp'
MYSQL_IP='192.168.66.30'
K8S_IP='192.168.66.20'
MYSQLPASS="sonar@123"

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
fi;

SHELL


end

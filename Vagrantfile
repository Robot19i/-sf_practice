Vagrant.configure("2") do |config|
  config.vm.box_check_update = false
  config.vm.box = "generic/ubuntu1804"
  config.vm.provision "file", source: "./exchange/file.txt", destination: "/home/vagrant/"
  config.vm.host_name = "py-host"
  config.vm.provider "virtualbox" do |vb|
  vb.memory = "1024"
end
    config.vm.provision "shell", inline: <<-SHELL   
	sudo apt-get -y update
	sudo apt-get -y install build-essential zlib1g-dev libpq-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev python3-dev    
    sudo apt-get -y install python3-pip    
	sudo pip3 install --upgrade pip
    sudo pip3 install psycopg2
    sudo pip3 install Django
    SHELL
	
end

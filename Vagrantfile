Vagrant.configure("2") do |config|
  (1..3).each do |i|
    config.vm.define "server#{i}" do |server|
      server.vm.box = "ubuntu/bionic64"  # Puedes usar otra versión de Ubuntu si prefieres
      server.vm.network "forwarded_port", guest: 22, host: 2200 + i
	  # por alguna razon esto de aqui no funciona y crea los ports 2222, 2200 y 2204
      server.vm.provider "virtualbox" do |vb|
        vb.memory = "256"
        vb.cpus = 1
      end
    end
  end
end
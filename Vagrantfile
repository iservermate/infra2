#WEB        SERVER
#NTP        SERVER 
#DB         SERVER
#SYSLOG     ESRVER
#DNS        SERVER
#MAIL       SERVER
#Repo        SERVER

#NAGIOS     CONTIANER
#JENKINS    CONTIANER
#LOGSTASH   CONTIANER/SERVER
#AWX        CONTAINER

Vagrant.configure("2") do |config|
    config.vm.box = "generic/centos8"

    #Repo SERVER
    # config.vm.define "repo" do |repo|
      # repo.vm.hostname = "repo.iservermate.local"
      # repo.vm.box_check_update = false
      # repo.vm.network "public_network", bridge: "eno1", ip:"192.168.0.91"
      # repo.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #repo.vm.provision "shell", path: "provisioners/packages.sh"
    # end

    #NTP SERVER
    config.vm.define "ntp" do |ntp|
      ntp.vm.hostname = "ntp.iservermate.local"
      ntp.vm.box_check_update = false
      ntp.vm.network "public_network", bridge: "eno1", ip:"192.168.0.92"
      ntp.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #ntp.vm.provision "shell", path: "provisioners/packages.sh"
    end

    #WEB SERVER
    config.vm.define "web" do |web|
      web.vm.hostname = "web.iservermate.local"
      web.vm.box_check_update = false
      web.vm.network "public_network", bridge: "eno1", ip:"192.168.0.93"
      web.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #web.vm.provision "shell", path: "provisioners/packages.sh"
    end

    #DB SERVER
    config.vm.define "db" do |db|
      db.vm.hostname = "db.iservermate.local"
      db.vm.box_check_update = false
      db.vm.network "public_network", bridge: "eno1", ip:"192.168.0.94"
      db.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #db.vm.provision "shell", path: "provisioners/packages.sh"
    end
 
    #MAIL SERVER
    config.vm.define "mail" do |mail|
      mail.vm.hostname = "mail.iservermate.local"
      mail.vm.box_check_update = false
      mail.vm.network "public_network", bridge: "eno1", ip:"192.168.0.95"
      mail.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #dns.vm.provision "shell", path: "provisioners/packages.sh"
    end
 
    #SYSLOG SERVER
    config.vm.define "syslog" do |syslog|
      syslog.vm.hostname = "syslog.iservermate.local"
      syslog.vm.box_check_update = false
      syslog.vm.network "public_network", bridge: "eno1", ip:"192.168.0.96"
      syslog.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #syslog.vm.provision "shell", path: "provisioners/packages.sh"
    end
 
    #DNS SERVER
    # config.vm.define "dns" do |dns|
      # dns.vm.hostname = "dns.iservermate.local"
      # dns.vm.box_check_update = false
      # dns.vm.network "public_network", bridge: "eno1", ip:"192.168.0.97"
      # dns.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #dns.vm.provision "shell", path: "provisioners/packages.sh"
    # end

    #NAGIOS SERVER
    config.vm.define "nagios" do |nagios|
      nagios.vm.hostname = "nagios.iservermate.local"
      nagios.vm.box_check_update = false
      nagios.vm.network "public_network", bridge: "eno1", ip:"192.168.0.98"
      nagios.vm.provision "file", source: "files/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
      #nagios.vm.provision "shell", path: "provisioners/packages.sh"
    end
 
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
    vb.cpus = "1"
  end
end

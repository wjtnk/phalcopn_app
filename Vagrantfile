Vagrant.configure("2") do |config|
  config.vm.box = "CentOS7"
  #ローカルでアクセスするときのIPアドレス。
  config.vm.network "private_network", ip: "192.168.50.10"
  #同期先を指定。「カレントディレクトリ（.）を/vagrant以下に同期」と、「syncディレクトリを/var/www/」以下に同期する。
  config.vm.synced_folder ".", "/vagrant"
  config.vm.synced_folder "sync", "/var/www/"
  config.vm.network "forwarded_port", guest: 80, host: 8080
end

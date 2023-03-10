# Linux_h_w.04
1. Подключить дополнительный репозиторий на выбор: Docker, Nginx, Oracle MySQL. Установить любой пакет из этого репозитория.

 	/etc/apt/sources.list.d# echo "deb http://nginx.org/packages/ubuntu focal nginx" >   nginx.list
      /etc/apt/sources.list.d# curl -fsSL https://nginx.org/keys/nginx_signing.key | sudo apt-key add -

      /etc/apt/sources.list.d# sudo apt update
	/etc/apt/sources.list.d# sudo apt install nginx -y



2. Установить и удалить deb-пакет с помощью dpkg.
  
      dpkg -i virtualbox-6.1_6.1.36-152435~Ubuntu~jammy.deb
	apt -f install
	deb [arch=amd64 signed-by=/usr/share/keyrings/oracle-virtualbox-2016.gpg] 	https://download.virtualbox.org/virtualbox/debian <mydist> contrib
	wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --dearmor --yes --output 	/usr/share/keyrings/oracle-virtualbox-2016.gpg
	dpkg -r virtualbox-6.1

3. Установить и удалить snap-пакет.

      sudo snap install robomongo
	sudo remove robomongo

4. Добавить задачу для выполнения каждые 3 минуты (создание директории, запись в файл).
  
  $ crontab -e
  */3 * * * * root mkdir /home/user/new. аргумент2
  


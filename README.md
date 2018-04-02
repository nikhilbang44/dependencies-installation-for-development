# crome install
	1. wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
	2. sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
	3. sudo apt-get update 
	4. sudo apt-get install google-chrome-stable
# node install
	1. sudo apt-get update
	2. sudo apt-get install nodejs
# npm install
	1. sudo apt-get install npm
# atom install
	1. sudo add-apt-repository ppa:webupd8team/atom
	2. sudo apt-get update
	3. sudo apt-get install atom
# mongo install
	1. sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 
	2. for ubuntu(14.04)
    	echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
	3. sudo apt-get update    
	4. sudo apt-get install -y mongodb-orsudo apt-get update

# Install Git on Linux
	1. sudo apt-get update
	2. sudo apt-get install git
# Git Branch With Colours In Bash Prompt
	# Add git branch if its present to PS1
	parse_git_branch() {
	 git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
	}
	if [ "$color_prompt" = yes ]; then
	PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[01;31m\]$(parse_git_branch)\[\033[00m\]\$'
	else
	 PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w$(parse_git_branch)\$ '
	fi
# PostgreSQL
	1. sudo apt-get update
	2. sudo apt-get install postgresql postgresql-contrib
# LAMP
	1.  sudo apt-get update
	2.  sudo apt-get -y install apache2 mysql-server php5-mysql php5 libapache2-mod-php5 php5-mcrypt
	3.  sudo mysql_install_db
	4.  sudo mysql_secure_installation
	5.  sudo nano /etc/apache2/mods-enabled/dir.conf
	6.  sudo service apache2 restart
	7.  echo '<?php phpinfo(); ?>' | sudo tee /var/www/html/info.php
	8.  sudo apt-get update
	9.  sudo apt-get install phpmyadmin
	10. sudo php5enmod mcrypt
	11. sudo service apache2 restart
	12. sudo nano /etc/apache2/conf-available/phpmyadmin.conf
	13. Add an AllowOverride All directive within the <Directory /usr/share/phpmyadmin>
	14. sudo service apache2 restart
	15. sudo nano /etc/apache2/apache2.conf
	16. Add the following line at the end. Include /etc/phpmyadmin/apache.conf
# Ruby with RVM
	1. sudo apt-get update
	2. sudo apt-get install curl
	3. \curl -L https://get.rvm.io | bash -s stable --ruby
	4. source ~/.rvm/scripts/rvm
	5. rvm requirements
	6. rvm install ruby
	7. rvm use ruby --default
	8. rvm rubygems current
	9. gem install rails
	10. sudo apt-get install ruby-dev
# JAVA
	1. sudo apt-get update
	2. sudo apt-get install default-jre
	3. sudo apt-get install default-jdk
# DBeaver
	1. sudo apt-get -f install
	2. sudo apt-get update
	3. wget http://dbeaver.jkiss.org/files/dbeaver-ce_latest_amd64.deb
	4. sudo dpkg -i dbeaver-ce_latest_amd64.deb
	5. sudo apt-get -f install
# Redis
	1. sudo apt-get update
	2. sudo apt-get install build-essential
	3. sudo apt-get install tcl8.5
	4. wget http://download.redis.io/releases/redis-stable.tar.gz
	5. tar xzf redis-stable.tar.gz
	6. cd redis-stable
	7. make
	8. make test
	9. sudo make install
	10. cd utils
	11. sudo ./install_server.sh

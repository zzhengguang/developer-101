# php 5

	sudo apt-get install software-properties-common
	sudo add-apt-repository ppa:ondrej/php
	
	sudo apt-get update
	sudo apt-get install php5.6
	
	
	
# Composer


	curl -sS https://getcomposer.org/installer | php
	sudo mv composer.phar /usr/local/bin/composer
	
	composer config -g repo.packagist composer https://packagist.phpcomposer.com
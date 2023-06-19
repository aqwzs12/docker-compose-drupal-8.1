cr:
	@echo "\033[92mCC DRUPAL\033[0m"
	vendor/bin/drush cr

cim:
	@echo "\033[92mCIM DRUPAL\033[0m"
	vendor/bin/drush cim -y

create-db:
	@echo "\033[92mCREATE DB DRUPAL\033[0m"
	vendor/bin/drush sql:create -y

drupal-updb:
	@echo "\033[92mUPDB DRUPAL\033[0m"
	vendor/bin/drush updb -y

drupal-upwd:
	@echo "\033[92mPASSWORD ADMIN "admin"\033[0m"
	vendor/bin/drush upwd admin admin

import-db: 
	@echo "\033[92mIMPORT DB DRUPAL\033[0m"
	vendor/bin/drush sqlc < dump.sql -y

composer:
	composer install


container-php-r:
	docker exec -it --user root php-drupal bash

container-php:
	docker exec -it php-drupal bash

container-nginx:
	docker exec -it nginx-drupal bash

first-install: composer create-db import-db cr drupal-updb cim cr drupal-upwd
# docker-compose-drupal-8.1


RUN docker-compose up -d to install the project

Add the database definition to your settings.php file
$databases['default']['default'] = array (
  'database' => 'drupal',
  'username' => 'root',
  'password' => 'root',
  'prefix' => '',
  'host' => 'database-drupal',
  'port' => '3306',
  'namespace' => 'Drupal\\mysql\\Driver\\Database\\mysql',
  'driver' => 'mysql',
  'autoload' => 'core/modules/mysql/src/Driver/Database/mysql/',
);

Put your dump on /var/www/html/app and run the command : make first-install
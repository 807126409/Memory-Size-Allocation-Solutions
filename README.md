# Memory-Size-Allocation-Solutions
To get the current memory_limit value, run:

php -r "echo ini_get('memory_limit').PHP_EOL;"
Try increasing the limit in your php.ini file (ex. /etc/php5/cli/php.ini for Debian-like systems):

; Use -1 for unlimited or define an explicit value like 2G
memory_limit = -1
Or, you can increase the limit with a command-line argument:

php -d memory_limit=-1 composer.phar require hwi/oauth-bundle php-http/guzzle6-adapter php-http/httplug-bundle
To get loaded php.ini files location try:

php --ini
Another quick solution:

php composer.phar COMPOSER_MEMORY_LIMIT=-1 require hwi/oauth-bundle php-http/guzzle6-adapter php-http/httplug-bundle
if above command doesn't run then run the following command 
php -d memory_limit=-1 composer.phar install

Or Direct read the below documentation for error expalaination
https://getcomposer.org/doc/articles/troubleshooting.md#memory-limit-errors

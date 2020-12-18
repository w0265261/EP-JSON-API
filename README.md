# EP-JSON-API
Mixture of PHP &amp; MySQL magic to create readable json files for any end-users needs.

## Requirements: 
* MySQL (prefer 8.0)
* PHP (prefer 7.4)
* WebServer (prefix nginx)

### Towny Requirements:
* Towny in MySQL Mode
* Towny 0.96.5.6

## Installation
1. Create a MySQL user that has READ/SHOW access only to your Towny Database.
   1. Run the command in Mysql, `CREATE USER 'api'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PASSWORD'`
   2. Run the command in Mysql, `GRANT SELECT,SHOW VIEW ON towny.* TO 'api'@'localhost';
2. Drag and drop `includes` and `towny` into your web servers directory.
   1. Configure `includes/config.php` by setting your Host, Username, Password, Database name and Mysql Port.
   2. Configure each `town.php, resident.php, nations.php` variables such as `$column = 'towny_nations';` to match your case sensitive database, some databases require you set this as `$column = 'TOWNY_NATIONS';`
3. Once configured properly, you should be able to visit your web servers address and call into the `town.php, resident.php, nations.php` files. For example, `http://localhost/towny/town.php`

##API Usage 
1. Read our documentation for EarthPol's api, (https://earthpol.github.io/dist/api.html)[https://earthpol.github.io/dist/api.html]

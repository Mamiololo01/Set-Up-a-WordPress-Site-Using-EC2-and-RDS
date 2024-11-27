
## SET UP DETAILS

Create RDS Database

Using the AWS console, create an RDS database with the following configurations:

Choose a database creation method: Standard create

Engine options: MySQL

Edition: MySQL Community

Version: MySQL 8.0.28

Templates: Free tier

DB instance class: db.t2.micro

DB instance identifier: wordpress

Run Progress Check

Skip

Install Apache and Dependencies

Connect to your Cloud Server webserver-01 and perform the following tasks:

Use the apt command to install: apache2 libapache2-mod-php php-mysql

Move the /wordpress folder into your /var/www directory

Move your /var/www/wordpress/000-default.conf file to /etc/apache2/sites-enabled/

Restart apache2ctl


Configure WordPress

Configure wp-config.php to connect to the RDS database we created.

Edit your /var/www/wordpress/wp-config.php file and replace 'localhost' by your own RDS endpoint on the line define('DB_HOST', 'localhost');

Save and close the file


Modify Security Groups

Modify your non-default security group to allow the EC2 instance to connect to the MySQL/Aurora RDS database.


Complete Wordpress Installation and Test

Visit the website and complete the installation, ensuring the website can be visited and the WordPress portal works.

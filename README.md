# Linux_Server_Configuration
A baseline installation of a secured Linux server and prepare it to host web applications.

## Access Info:
* IP Address: 13.233.64.144
* SSH Port: 2200

## Web appication:
* URL: <a href="http://13.233.64.144.xip.io"> Web application </a> 

## Third-party resources:
* Create an account in <a href="https://lightsail.aws.amazon.com">Amazon Lightsail </a>
* Create an instance. Choose an instance image Ubuntu and give it a hostname.
* The public IP address of the instance is displayed along with its name.
* Download your default private key from the Account page.

## Configuration changes:
* Update and upgrade all Ubuntu packages using ```sudo apt-get update``` and ```sudo apt-get upgrade```
* Add new user named grader ```sudo adduser grader``` with password grader1.
* Add grader user to sudoer file ```sudo visudo```
* Add grader grader  ALL=(ALL:ALL) ALL
* Before enabling ufw ```sudo ufw enable``` allow ports ```2200/tcp, 80/tcp and 123/udp```.
* Generate key pair on a local machine with passphrase Udacity .
* Place the buplic key into a new directory called ~/.ssh
* Change the permission of .ssh and the buplic key file ```sudo chmod 700 ~/.ssh``` and ```sudo chmod 644 ~/.ssh/authorized_keys```.
* Disable password authentication by using ```sudo nano /etc/ssh/sshd_config```.
* Restart SSH service by using ```sudo service ssh restart```.
* Install Apache web server by using ```sudo apt-get install apache2```.
* Install mod_wsgi by using ```sudo apt-get install libapache2-mod-wsgi```.
* Install PostgreSQL by using ```sudo apt-get install postgresql```.
* Install ```git, flask, requests, oauth2client, sqlalchemy```
* Clone the category repository <a href="https://github.com/abualdana/Catalog.git"> Category </a>
* Connect to PostgreSQL by using ```engine = create_engine('postgresql://catalog:catalog@localhost/companycars')```.
* Run the seeder.py
* Run the application

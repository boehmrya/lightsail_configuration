# lightsail_configuration


## IP Address
52.3.221.91

## SSH Port
2200

## Software Installed

### Ubuntu Packages
finger

python2

postgresql

apache2

python-pip

git

libapache2-mod-wsgi

### Pip Packages
psycopg2

sqlalchemy

werkzeug==0.8.3

flask==0.9

Flask-Login==0.1.3

oauth2client

requests

httplib2

virtualenv

(also installed all of these packages in the virtual host at /var/www/catalog/catalog/venv)


## Summary of Configuration Changes
Upgraded all existing packages

Changed ssh port in /etc/ssh/sshd_config file to 2200

Via the firewall (UFW) enabled SSH (port 2200), HTTP (port 80), and NTP (port 123).

Created new user grader

Added ssh public key for grader in /home/grader/.ssh/authorized_keys

Enable sudo privileges for grader via modifications to /etc/sudoers.d/grader

Turned password authentication off and prevented root login in /etc/ssh/sshd_config file

Configured the local timezone to UTC

Added virtual host in /etc/apache2/sites-available/catalog.conf

Configured wsgi file at /var/www/catalog/catalog.wsgi

## Third Party Resources Used
Here were some useful threads that helped me:

https://serverfault.com/questions/265410/ubuntu-server-message-says-packages-can-be-updated-but-apt-get-does-not-update

http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/#creating-a-wsgi-file

https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps

In general the digital ocean documentation was very helpful in understanding server configuration better.  Also, the ubuntu packages website, the flask documentation, and stack overflow were critical.

https://www.digitalocean.com/community/tutorials

https://packages.ubuntu.com/

http://flask.pocoo.org/docs/1.0/

https://stackoverflow.com/questions/tagged/ubuntu


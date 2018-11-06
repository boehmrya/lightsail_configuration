# lightsail_configuration


## IP Address
52.3.221.91


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

Turned password authentication off in /etc/ssh/sshd_config file

Configured the local timezone to UTC

Added virtual host in /etc/apache2/sites-available/catalog.conf

Configured wsgi file at /var/www/catalog/catalog.wsgi

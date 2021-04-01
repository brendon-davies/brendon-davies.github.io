


common table expression

windows functions







if mysql gets borked with this error, here's how to fix it:

ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock' (2)

in vagrant:

sudo su

sudo pkill mysqld

sudo pkill mysql

sudo apt-get remove percona-server*

sudo apt-get purge percona-server*

sudo chef-client 

when i ran sudo chef-client i got these errors, but i just went on and it still worked


sudo service mysql restart

mysql

should now be fixed
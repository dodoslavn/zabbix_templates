# Zabbix template - Apache2 vhosts
This template for Zabbix to monitor in a basic way all vhosts which you have enabled in your Apache2 web server. It will list all server names from vhosts and generate several items for each.  
One vhost can contain only one domain.
# Instalation
- enable User Parameters in Zabbix agent configration
- add this User Parameter into Zabbix agent configuration
  - > UserParameter=custom.apache_vhosts,/bin/grep ServerName /etc/apache2/sites-enabled/*ssl.conf | /bin/sed 's/.*ServerName //'
  - make sure path to "grep" and "sed" Linux commands are correct, modify in line above if not
- import the template in Zabbix GUI
- open Host in Zabbix GUI
  - link the template

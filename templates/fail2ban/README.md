# Zabbix template - Fail2Ban / iptables
This template for Zabbix is to monitor amount of banned IP addresses by Fail2Ban tool adn iptables
# Instalation
- install package Fail2ban on system with Zabbix Agent adn make sure you use iptables
  - Debian
    - > apt install fail2ban
- test if it work based on output of iptables
  - > iptables -L -n
- allow custom scripts in Zabbix Agent
- add new UserParameter into Zabbix Agent config file (see UserParam.conf file)
- import the template in Zabbix GUI
- open Host in Zabbix GUI
  - link the template

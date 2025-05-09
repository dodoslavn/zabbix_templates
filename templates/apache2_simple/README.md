# Zabbix template - Apache2 - simple
This template for Zabbix is intended to monitor all Apache2 instances and to create HTTP agent for each domain used in virtual hosts
# Instalation
- install "jq" utility on your system
  - Debian
    - >apt install jq
- add new UserParameter into Zabbix Agent config file
  - see UserParam.conf file
- import the template in Zabbix GUI
- open Host in Zabbix GUI
  - link the template

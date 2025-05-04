# Zabbix template - Fail2Ban / iptables
This template for Zabbix is intended to get all values which tool lm-sensors report, and monitor them. Naturally, this is intended to work on physical servers, as there is no temperature to monitor on usual VM. Package lm-sensors, which provide "sensors" command is available on Linux (probably, only on Linux).
# Instalation
- install package lm-sensors on system with Zabbix Agent
  - Debian
    - > apt install lm-sensors
- test if the utility works and what it reports
  - > sensors
- allow custom scripts in Zabbix Agent
- add new UserParameter into Zabbix Agent config file (or see UserParam.conf file)
  - > UserParameter=custom.sensors,/usr/bin/sensors -j
- import the template in Zabbix GUI
- open Host in Zabbix GUI
  - link the template
  - add Macro with name "{$SENSORS.CPUPATH}" and value in format like this
    - > $['k10temp-pci-00c3']['temp1']['temp1_input']

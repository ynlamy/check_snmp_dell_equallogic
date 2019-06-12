This plugin can check the status of Dell EqualLogic storage using SNMP queries.

check_snmp_dell_equallogic is written in Bash and is distributed under the GPLv2 license. This plugin have been created by Yoann LAMY.

Usage: ./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t redundancy

-H ADDRESS
Name or IP address of host (default: 127.0.0.1)
-C STRING
Community name for the host's SNMP agent (default: public)
-n STRING"
Member name
-t STRING
Check type (battery, connection, controller, disk, fan, health, info, io, latency, network, redundancy, temperature, usage, raid, volume) (default: info)
-i STRING
Network interface (default: eth0)
-m INTEGER
MTU size (default: 9000)
-s INTEGER
Network interface speed (default: 1000)
-d INTEGER
Disk number (default: 1)
-v STRING
Volume name (default: vss-control)
-w INTEGER
Warning level for size in percent (default: 0)
-c INTEGER
Critical level for size in percent (default: 0)
-h
Print this help screen
-V
Print version and license information

This plugin uses 'snmpget' and 'snmpwalk' commands included with the NET-SNMP package.
This plugin support performance data output (connection, fan, io, latency, temperature, usage, volume).

Examples :

./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t battery
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t connection -w 15 -c 20
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t controller
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t disk -d 1
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t fan
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t health
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t io -w 2000 -c 3000
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t latency
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t network -i eth0 -m 9000 -s 1000
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t redundancy
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t raid
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t temperature
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t usage -w 90 -c 95
./check_snmp_dell_equallogic -H xxx.xxx.xxx.xxx -C public -n BAIE01 -t volume -v volume01 -w 90 -c 95

This nagios plugins comes with ABSOLUTELY NO WARRANTY.

You may redistribute copies of the plugins under the terms of the GNU General Public License v2.

# icinga-tools
Some icinga tools

**analyze-hosts**

Analyzes the host configuration and groups the hosts with identical configuration. "Configuration" here are the fields from 'Max. Check Attempts' to the end of each line.

Example output (stripped output):
```
Config: '10';'0h 5m 0s';'0h 1m 0s';'check-host-alive_ipv6';'24x7';'Yes';'Yes';'Yes';'No';'Auto-determined value';'admins';'20h 0m 0s';'0h 0m 0s';'Down, Unreachable, Recovery';'24x7';'';'Yes';'None';'Yes';'Program-wide value';'Program-wide value';'Up, Down, Unreachable';'Yes';'Yes';'';'Notes ersetzt*';'';'/pnp4nagios/graph?host=$HOSTNAME$';'';'';'';'';'';'';'Status Information, Non-Status Information'
Used by: 42 hosts
Hosts: 'host1', 'host2', ...
```

Steps:
- In Icinga Classic View, go to Configuration/View Config, select Host (Continue)
- Export data using CSV format (upper right corner)
- Save the file
- Run perl script (CSV file in same directory)


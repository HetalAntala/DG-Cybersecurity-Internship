# Day 78 – CPU & Disk Alerts in Nagios

CPU load and disk usage alerts were configured using check_load and
check_disk plugins. Initial configuration failed due to missing command
definitions. After defining commands in commands.cfg and validating
plugins, Nagios successfully monitored system resources.

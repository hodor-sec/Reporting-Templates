**Command**
$ sudo nmap -sU -p 161 --open -Pn -n -iL ../osint/ipv4info/all_individual_ip.txt -oN nmap.snmp-all_ip.txt -oG nmap.snmp-all_ip-grep.txt


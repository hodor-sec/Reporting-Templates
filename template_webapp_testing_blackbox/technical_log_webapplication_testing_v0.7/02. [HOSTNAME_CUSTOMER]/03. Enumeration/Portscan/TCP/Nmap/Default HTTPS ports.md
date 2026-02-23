**Command**
$ sudo nmap -iL cidr_ip_ranges.txt -Pn -n -p 443,444,4443,8443 -T4 --max-rtt-timeout 200ms --initial-rtt-timeout 150ms --min-hostgroup 512 -v --open -oN nmap.tcpconnect.https-ports-default.txt -oG nmap.tcpconnect.https-ports-default-grep.txt
$ grep open nmap.tcpconnect.https-ports-default-grep.txt  | awk {'print $2'} | egrep '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' | sort -n -t"." -k1,3 | uniq > https-ports.txt

**Output**

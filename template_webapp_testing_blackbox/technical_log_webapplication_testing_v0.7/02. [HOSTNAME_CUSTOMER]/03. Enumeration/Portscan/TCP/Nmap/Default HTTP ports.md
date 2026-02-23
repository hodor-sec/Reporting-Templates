**Command**
$ sudo nmap -iL cidr_ip_ranges.txt -Pn -n -p 80,8080,8880,8088,8888 -T4 --max-rtt-timeout 200ms --initial-rtt-timeout 150ms --min-hostgroup 512 -v --open -oN nmap.tcpconnect.http-ports-default.txt -oG nmap.tcpconnect.http-ports-default-grep.txt
$ grep open nmap.tcpconnect.http-ports-default-grep.txt  | awk {'print $2'} | egrep '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' | sort -n -t"." -k1,3 | uniq > http-ports.txt

**Output**

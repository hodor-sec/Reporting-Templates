**Command**
$ nmap -sn -Pn -n -iL cidr_ip_ranges.txt -oN nmap.generate-ip.txt
$ grep report nmap.generate-ip.txt | awk {'print $5'}
$ grep report nmap.generate-ip.txt | awk {'print $5'} > all_individual_ip.txt

**Output**

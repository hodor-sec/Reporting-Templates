**Command**
$ for range in $(cat ../cidr_ip_ranges.txt); do nmap -sn -Pn -n -oN nmap.generate-ip-$(printf "%s" "$range" | sed -e 's/\/.*//').txt $range; done
$ for range in $(ls -1 nmap.generate-ip-*.txt); do egrep 'report for' $range | awk {'print $5'} > ip_range_$range; done
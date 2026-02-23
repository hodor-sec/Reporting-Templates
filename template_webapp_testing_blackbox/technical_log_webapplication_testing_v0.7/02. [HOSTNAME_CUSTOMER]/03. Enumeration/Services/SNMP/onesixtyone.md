**Command**
$ for range in $(cat cidr_ip_ranges.txt); do nmap -sn -Pn -n $range | grep 'report for' | awk {'print $5'} | tee ip_range_nmap.generate-ip-${range%???}.txt; done
$ for range in $(ls -1 ip_range_nmap.generate-ip*.txt); do onesixtyone -i $range; done

**Output**

**Command**
$ for range in $(cat ip_ranges.txt); do ipcalc $range | tail -n 1; done | sort -n -t"." -k1,3 | uniq
$ for range in $(cat ip_ranges.txt); do ipcalc $range | tail -n 1; done | sort -n -t"." -k1,3 | uniq > cidr_ip_ranges.txt

**Output**

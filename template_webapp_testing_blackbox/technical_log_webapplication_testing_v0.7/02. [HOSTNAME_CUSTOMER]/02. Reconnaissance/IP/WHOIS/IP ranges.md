**Command:**
$ for range in $(cat cidr_ip_ranges_no_suffix.txt); do echo $range; printf '\n'; whois -H $range | egrep 'NetName:|Organization:'; printf '\n'; done | tee whois_ip_ranges.txt

**Output:**

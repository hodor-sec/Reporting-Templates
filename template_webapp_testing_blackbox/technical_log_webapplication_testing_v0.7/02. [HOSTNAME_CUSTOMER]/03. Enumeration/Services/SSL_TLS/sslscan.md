**Command:**
for fqdn in $(cat fqdn.txt); do echo $fqdn; printf "\n"; timeout 180 sslscan $fqdn | aha --black > sslscan_${fqdn}.html; done

**Output:**

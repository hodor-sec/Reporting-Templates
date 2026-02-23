**Command:**
for fqdn in $(cat fqdn.txt); do echo $fqdn; printf "\n"; timeout 180 testssl $fqdn | aha --black > testssl_$fqdn.html; done

**Output:**

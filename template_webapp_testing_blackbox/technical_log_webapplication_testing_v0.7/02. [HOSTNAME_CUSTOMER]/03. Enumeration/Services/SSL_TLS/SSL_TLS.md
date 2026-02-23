**Command:**
for fqdn in $(cat /tmp/fqdn.txt); do echo $fqdn; printf "\n"; timeout 180 bash testssl.sh $fqdn | aha --black > /tmp/testssl_$fqdn.html; done

**Output:**


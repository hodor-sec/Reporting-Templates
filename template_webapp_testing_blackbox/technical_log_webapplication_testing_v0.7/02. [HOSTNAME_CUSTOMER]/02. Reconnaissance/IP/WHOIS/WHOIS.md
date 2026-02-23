**Command:**
for ip in $(cat ip.txt); do echo $ip; printf "\n"; whois -H $ip | egrep -v '%|#'; printf "\n";done

**Output:**
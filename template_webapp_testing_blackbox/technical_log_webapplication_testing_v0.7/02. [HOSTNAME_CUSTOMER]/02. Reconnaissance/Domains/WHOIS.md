**Command:**
for domain in $(cat domain.txt); do echo $domain; printf "\n"; whois -H $domain | egrep -v '%|#'; printf "\n";done

**Output:**
**Command:**
for fqdn in $(cat fqdn.txt); do dig $fqdn | grep -A1 'ANSWER SECTION' | grep -v ANSWER;done

**Output:**

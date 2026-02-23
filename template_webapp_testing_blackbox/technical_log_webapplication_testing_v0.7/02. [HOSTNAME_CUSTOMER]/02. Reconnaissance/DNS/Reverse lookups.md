**Command:**
$ for ip in $(cat all_individual_ip.txt); do dig -x $ip | grep -A1 'ANSWER SECTION' | grep -v ANSWER;done | tee reverse_lookups_all_individual_ip.txt

**Output:**

**Command**
$ nmap -sn -Pn -iL fqdns.txt -oN nmap.fqdns.resolvable.txt -oG nmap.fqdns.resolvable-grep.txt
$ grep 'report for' nmap.fqdns.resolvable.txt | awk {'print $5'}

**Output**

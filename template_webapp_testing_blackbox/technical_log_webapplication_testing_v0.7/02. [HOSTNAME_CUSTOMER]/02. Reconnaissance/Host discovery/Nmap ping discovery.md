**Command**
$ cat nmap.uphosts-cidr-ipranges-grep.txt | egrep Up | awk {'print $2'}
$ cat nmap.uphosts-cidr-ipranges-grep.txt | egrep Up | awk {'print $2'} > nmap_uphosts.txt

**Output**

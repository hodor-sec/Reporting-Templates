Copy IPv4info tables in HTML to TXT file -> raw_data.txt

**Command**
$ cat raw_data.txt | egrep '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' | awk {'print $1 "-" $2'}
$ cat raw_data.txt | egrep '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' | awk {'print $1 "-" $2'} > ip_ranges.txt

**Output**

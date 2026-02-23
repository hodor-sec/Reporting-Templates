**Script oneliner:**
for domain in $(cat domains.txt); do printf "\n"; curl -s https://crt.sh/?q=%25.${domain} | html2text | grep $domain | awk {'print $5'} | uniq | sort | uniq; printf "\n";done

**Output:**

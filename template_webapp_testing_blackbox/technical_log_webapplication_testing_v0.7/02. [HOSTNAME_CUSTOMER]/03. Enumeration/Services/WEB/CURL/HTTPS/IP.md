**Command:**
for ip in $(cat https-ports.txt); do for port in $(printf "443\n444\n4443\n8443"); do echo $ip:$port; printf "\n"; timeout 3 curl -L -k -I -X GET https://$ip:$port; done; done | tee curl_https_ip.txt 
cat curl_https_ip.txt | grep --color=always -E '^|^[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}:[0-9]{1,6}$' | aha --black > curl_https_ip.html

**Output:**

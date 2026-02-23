**Command:**
for ip in $(cat http-ports.txt); do for port in $(printf "80\n8080\n8880\n8088\n8888"); do echo $ip:$port; printf "\n"; timeout 3 curl -L -k -I -X GET http://$ip:$port; done; done | tee curl_http_ip.txt
cat curl_http_ip.txt | grep --color=always -E '^|^[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}:[0-9]{1,6}$' | aha --black > curl_http_ip.html

**Output**

**Command:**
for fqdn in $(cat osint-resolvable.txt); do for port in $(printf "80\n8080\n8880\n8088\n8888"); do echo $fqdn:$port; printf "\n"; timeout 3 curl -L -k -I -X GET http://$fqdn:$port; done; done | tee curl_http_fqdn.txt
cat curl_http_fqdn.txt | grep --color=always -E '^|^(([a-zA-Z0-9]|[a-zA-Z0-9][a-zA-Z0-9\-]*[a-zA-Z0-9])\.){1,}([A-Za-z0-9]|[A-Za-z0-9][A-Za-z0-9\-]*[A-Za-z0-9]){1,}:[0-9]{1,6}$' | aha --black > curl_http_fqdn.html

**Output:**

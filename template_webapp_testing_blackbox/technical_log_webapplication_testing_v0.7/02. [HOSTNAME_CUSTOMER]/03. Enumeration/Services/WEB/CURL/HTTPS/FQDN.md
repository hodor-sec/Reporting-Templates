**Command:**
for fqdn in $(cat osint-resolvable.txt); do for port in $(printf "443\n444\n4443\n8443"); do echo $fqdn:$port; printf "\n"; timeout 3 curl -L -k -I -X GET https://$fqdn:$port; done; done | tee curl_https_fqdn.txt
cat curl_https_fqdn.txt | grep --color=always -E '^|^(([a-zA-Z0-9]|[a-zA-Z0-9][a-zA-Z0-9\-]*[a-zA-Z0-9])\.){1,}([A-Za-z0-9]|[A-Za-z0-9][A-Za-z0-9\-]*[A-Za-z0-9]){1,}:[0-9]{1,6}$' | aha --black > curl_https_fqdn.html

**Output:**

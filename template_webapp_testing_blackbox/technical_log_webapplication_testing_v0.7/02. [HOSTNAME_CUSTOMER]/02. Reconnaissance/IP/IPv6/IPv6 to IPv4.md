**Map remote IPv6 port 80 to local IPv4 8080**
socat TCP-LISTEN:8080,reuseaddr,fork TCP6:[fe80::6bb8:7dff:fe40:7527]:80


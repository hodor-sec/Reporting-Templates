**Active discovery**
ping6 -I eth0 -c 5 ff02::1 > /dev/null
ip -6 neigh

**Passive discovery**
detect-new-ip6 eth0
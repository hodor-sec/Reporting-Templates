modprobe 8021q
vconfig add eth0 100
ifconfig eth0.100
dhclient eth0.100
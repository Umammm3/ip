# DNS Mikrotik 
ip dns set allow-remote-request=yes
ip dns static add name=umam.sch.id address=36.36.36.5 (ip debian)
ip firewall nat add chain=dstnat protocol=udp dst-port=53 action=dst-nat to-port=53 to-address=36.36.36.1 (ip Mikrotik)
ip dns cache flush 

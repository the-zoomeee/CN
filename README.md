# CN

## router config
```
en
config t
hostname R1
int fa 0/0
ip add 192.168.1.1 255.255.255.0
no shut

int Serial0/0/0
ip add 12.0.0.3 255.255.255.252
clock rate 64000
no shut
```

## static route
en
config t
hostname R1
ip route 192.168.1.0 255.255.255.0 10.0.0.0
ex

## RIP route
en
config t
hostname R1
router rip
network 192.168.1.0 (all connected adjacent devices)
ex


## OSPF route
en
config t
hostname R1
router ospf 1
network 192.168.1.0 0.0.0.255 area 0



## DHCP pool
en
config t
hostname R1
ip dhcp pool aa
network (router ip) (subnet mask)
default-router (getway)
dns-server (dns ip)
ex
ip dhcp excluded-address 10.0.0.2 10.0.0.10
ex

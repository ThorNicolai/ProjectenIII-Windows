# Configuratie van Router 4

```
enable
erase startup-config
y
delete vlan.dat
yes
y
configure terminal
no ip domain-lookup
hostname Router4
enable secret project3
line console 0
password project3
exec-timeout 5
login
exit
line vty 0 15
password project3
exec-timeout 5
transport input ssh
login 
exit
interface S0/1/0
ip address 192.0.2.13 255.255.255.252
no shutdown
interface g0/1
ip address 192.0.2.17 255.255.255.252
no shutdown
end
configure terminal
router rip
version 2
default-information originate
network 192.0.2.12
network 192.0.2.16
passive-interface serial 0/1/0
end
write
```
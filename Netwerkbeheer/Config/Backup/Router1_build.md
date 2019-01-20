# Configuratie van Router 1

```
enable
erase startup-config
y
delete vlan.dat
yes
y
configure terminal
no ip domain-lookup
hostname Router1
enable secret teamred
line console 0
password project3
exec-timeout 5
login
exit
service password-encryption
line vty 0 15
password project3
exec-timeout 5
login
exit

configure terminal
interface g0/1
ip address 172.18.0.73 255.255.255.252
no shutdown
interface g0/0
ip address 192.0.2.6 255.255.255.252
no shutdown
end

configure terminal
router rip
version 2
default-information originate
network 192.0.2.4
network 172.18.0.0
end
write


```

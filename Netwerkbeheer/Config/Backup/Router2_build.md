# Configuratie van Router 2

```
enable
erase startup-config
y
delete vlan.dat
yes
y
configure terminal
no ip domain-lookup
hostname Router3
enable secret teamgreen
line console 0
password project3
exec-timeout 5
login
exit
username admin secret teamred
service password-encryption
line vty 0 15
password project3
exec-timeout 5
login
transport input ssh
exit

configure terminal
interface g0/1
ip address 192.0.2.1 255.255.255.252
no shutdown
interface S0/1/1
ip address 192.0.2.9 255.255.255.252
no shutdown
interface s0/1/0
ip address 192.0.2.14 255.255.255.252
no shutdown
end

configure terminal
router rip
version 2
default-information originate
network 192.0.2.0
network 192.0.2.8
network 192.0.2.12
end
write
```
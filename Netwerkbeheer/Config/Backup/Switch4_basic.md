# Configuratie van Switch 4

```
enable
erase startup-config
y
delete vlan.dat
yes
y
configure terminal
no ip domain-lookup
hostname Switch4
enable secret teamred
line console 0
password project3
exec-timeout 5
login
exit
username admin secret teamred
service password-encryption
ip domain-name red.local
crypto key generate rsa
1024
line vty 0 15
login local
transport input ssh
ip ssh version 2
end
copy running-config startup-config
y
exit
```

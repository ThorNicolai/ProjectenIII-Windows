# Configuratie van Switch 5
```

int vlan 200
ip address 172.18.2.1 255.255.255.128
no shutdown
int g0/1
no sw
ip add 172.18.0.70 255.255.255.252
no shut
int vlan 300
ip add 172.18.0.1 255.255.255.224
no shut
exit
router rip
version 2
network 172.18.0.64
end
write
```

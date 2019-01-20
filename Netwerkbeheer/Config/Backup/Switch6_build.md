# Configuratie van Switch 6

```
int Fa0/5
ip add 172.18.0.33 255.255.255.224
no shut
int g0/1
no switchport
ip add 172.18.0.70 255.255.255.252
no shut
int g0/2
no switchport
ip add 172.18.0.65 255.255.255.252
no shut
exit
router rip
version 2
network 172.18.0.32
network 172.18.0.64
end
write
```

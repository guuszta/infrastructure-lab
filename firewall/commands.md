# 🔢 Comandos utilizados para configuração inicial do Firewall

1. Acesso administrativo  

```
config system global  
    set admin-sport 443  
end
```

2. Configuração da Interface WAN (port1)  

```
config system interface  
    edit port1  
        set mode dhcp  
        set allowaccess ping https ssh  
    next  
end
```

3. Configuração da Interface LAN (port2)  

```
config system interface  
    edit port2  
        set ip 192.168.0.1/24  
        set allowaccess ping https ssh  
    next  
end
```

4. DHCP Server (LAN)  

```
config system dhcp server  
    edit 1  
        set interface port2  
        set default-gateway 192.168.0.1  
        set netmask 255.255.255.0  
        config ip-range  
            edit 1  
                set start-ip 192.168.0.100  
                set end-ip 192.168.0.200  
            next  
        end  
        set dns-server1 192.168.0.2  
        set dns-server2 1.1.1.1  
    next  
end
```

5. Política LAN to WAN (com NAT)  

```
config firewall policy  
    edit 1  
        set srcintf port2  
        set dstintf port1  
        set action accept  
        set srcaddr all  
        set dstaddr all
        set schedule always
        set service ALL
        set nat enable  
    next  
end
```



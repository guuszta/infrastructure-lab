# 📌 Visão Geral Do Firewall

Este diretório documenta o Firewall utilizado no ambiente, baseado no Fortigate (FortiOS). Configurações gerais de rede e explicações estão documentadas em: [Network](https://github.com/guuszta/infrastructure-lab/blob/dev/network/README.md)

## 🌐Interfaces configuradas

### Porta 1 (WAN)

NIC: NAT  
IP WAN: Dynamic IP (VMWare NAT IP)

### Porta 2 (LAN)

NIC: LAN Segment 1  
IP LAN: 192.168.0.1/24 

### DHCP

Range: 192.168.0.100 - 192.168.0.200  
Mask: 255.255.255.0  
Gateway: 192.168.0.1  
DNS: 192.168.0.2 (Windows Server)  
DNS alt: 1.1.1.1

## ⛔ Políticas

### LAN-to-WAN (SNAT)  

Source Interface: port2 (LAN)  
Destination Interface: port1 (WAN)

Action: Accept  
Source Address: all  
Destination Address: all  
Schedule: always  
Services: ALL  
NAT: enabled




# 📌 Visão Geral Do Firewall

Este diretório documenta o Firewall utilizado no ambiente, baseado no Fortigate (FortiOS). Configurações gerais de rede e explicações estão documentadas em: [Network](https://github.com/guuszta/infrastructure-lab/blob/dev/network/README.md)

## 🌐Interfaces configuradas

### Porta 1 (WAN)

IP WAN: Dynamic IP (VMWare NAT)

### Porta 2 (LAN)

192.168.0.1/24  
LAN Segment 1

### DHCP

Range: 192.168.0.100 - 192.168.0.200  
Máscara: 255.255.255.0  
Gateway: 192.168.0.1
DNS: 192.168.0.2 (Windows Server)  
DNS alt: 1.1.1.1

## 🧬Protocolos habilitados

- NAT
- DHCP
- HTTP/HTTPS
- SSH
- PING

## ♒Fluxos principais

- LAN → WAN (NAT)
- LAN → AD/DNS
- LAN → DB
- LAN → Client Hosts

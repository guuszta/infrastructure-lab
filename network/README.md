# 📌 Rede Virtual Do Projeto

Este diretório contém todas as informações sobre a rede do projeto, desde informações técnicas, quanto explicações visuais e escritas do caminho de tráfego.

## 🌐 Informações técnicas

### Firewall

*Porta 1* (WAN)

IP WAN: 192.168.186.131 (VMWare NAT)  

<br>

*Porta 2* (LAN)

192.168.0.1/24 (LAN Segment 1)

<br>

*DHCP*

IP Range: 192.168.0.100 - 192.168.0.200  
IP Mask: 255.255.255.0  
Gateway: 192.168.0.1 (Firewall)  
DNS: 192.168.0.2 (Windows Server)  
DNS alt: 1.1.1.1

<br>

### Infraestrutura

Sub-rede: 192.168.0.0/24

Firewall: 192.168.0.1

Windows Server 2019: 192.168.0.2

Ubuntu Server: 192.168.0.3

Hosts Reservados: 192.168.0.4 - 192.168.0.99

Windows 11 / Outros Hosts: <Dynamic IP>

<br>

## 💬 Topologia Descrita

 O início da rede ocorre pela **Porta 1** do Firewall, que está conectada ao modo **NAT** do VMware Workstation. Nesse modo, o VMware entrega ao Firewall um endereço **WAN via DHCP**, permitindo acesso à internet e funcionando como uma WAN interna exclusiva para o laboratório.

 A **Porta 2** do Firewall é configurada como a **LAN** de toda a rede virtual, vinculada ao **LAN Segment 1** no VMware. A partir disso, é criada uma política **LAN to WAN**, permitindo que o tráfego da rede interna saia para a porta WAN. Esse fluxo gera um **Double NAT**, consequência da combinação do NAT do VMware com o NAT do próprio Firewall. Criando um cenário onde posso simular uma rede local real, onde um Firewall controla o tráfego de toda a rede.

 Todos os adaptadores de rede das VMs estão vinculados ao **LAN Segment 1**, sendo totalmente controlados pelo Firewall. Dessa forma, as VMs acessam a internet por meio do NAT do Firewall e se comunicam entre si por estarem no mesmo domínio de broadcast, dentro da mesma sub-rede. Cada VM utiliza endereçamento estático conforme documentado nas Informações Técnicas.

## 🆔 Convenção De Nomes

Firewall: ***FW01***

Windows Server 2019: ***SRV-DC***

Ubuntu Server: ***SRV-DB***

Windows 11: ***CLIENT-01***

Domínio: **infralab.local**

FQDN Do DC: **srv-dc.infralab.local**

# 🧱 Infrastructure Lab — On-Premise

Este repositório documenta um laboratório de infraestrutura on-premise, desenvolvido com foco em redes, firewall, servidores e serviços corporativos, simulando um ambiente real de produção.

O projeto foi construído em ambiente virtualizado utilizando **VMware Workstation**, com controle centralizado de rede via **Firewall Fortigate**.

<br>

## 🎯 Objetivo do Projeto

- Simular uma infraestrutura corporativa real
- Consolidar conhecimentos práticos em:
  - Firewall e NAT
  - Active Directory e DNS
  - Servidores
- Criar material técnico documentado para **portfólio profissional**

<br>

## 🗺️ Topologia Lógica da Rede

![Topologia Lógica](https://github.com/guuszta/infrastructure-lab/blob/dev/network/Topologia-Logica.jpeg)

### Visão Geral
- Firewall Fortigate como gateway da rede
- **NAT** para acesso à internet
- **DHCP** para máquinas clientes
- Servidores e clientes na mesma LAN
- Controle de tráfego via políticas de firewall

<br>

## 🧩 Componentes do Ambiente

### 🧱 Firewall
- Fortigate (FortiOS)
- NAT (SNAT)
- DHCP Server
- Políticas LAN → WAN
- Controle de acesso por interface

📁 Documentação: [`/Firewall`](https://github.com/guuszta/infrastructure-lab/tree/main/firewall)

<br>

### 💻 Windows Server
- Active Directory Domain Services (AD DS)
- DNS integrado ao domínio
- GPOs básicas
- Autenticação centralizada

📁 Documentação: [`/Servers/Windows-Server`](https://github.com/guuszta/infrastructure-lab/tree/main/servers/windows-server-2019)

<br>

### 🐧 Ubuntu Server
- MySQL Server (Dedicated)
- Acesso remoto controlado
- Integração com cliente Windows

📁 Documentação: [`/Servers/Ubuntu-Server`](https://github.com/guuszta/infrastructure-lab/tree/main/servers/ubuntu-db)

<br>

### 💻 Windows 11
- IP dinâmico via DHCP
- Ingressado no domínio
- Acesso ao MySQL via MySQL Workbench

📁 Documentação: [`/Clients/Windows-11`](https://github.com/guuszta/infrastructure-lab/tree/main/servers/windows11)

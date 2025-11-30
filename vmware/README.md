# 📌Ambiente De Virtualização Do Projeto  
Este diretório contém toda a estrutura e documentação relacionada as máquinas virtuais utilizadas no laboratório de infraestrutura. O software de virtualização a ser utilizado será o VMWare Workstation.


## 🖥️Máquinas Virtuais
* FortigateOS (NAT, DHCP, Políticas, etc.);  
* Windows Server 2019 (AD/DNS);  
* Ubuntu Server (MySQL Dedicated Server);  
* Windows 11 (Host Cliente).


## ⚙️Configuração de Hardware das VMs

### 🧱Fortigate OS
* 1 CPU
* 1 GB RAM
* 2 NICs (WAN/LAN)

### 🪟Windows Server 2019
* 2 CPU
* 2 GB RAM
* 1 NIC

### 🐧Ubuntu Server
* 2 CPU
* 2 GB RAM
* 1 NIC

### 🖥️Windows 11
* 2 CPU
* 4 GB RAM
* 1 NIC

## 🌐Configuração De Rede Virtual (vNICs)

### 🧱Fortigate OS
NIC1 (WAN): Modo NAT  
NIC2 (LAN): Lan Segment 1

### 🪟Windows Server 2019
NIC: Lan Segment: 1  

### 🐧Ubuntu Server (MySQL)
NIC: Lan Segment: 1

### 🖥️Windows 11 Client
NIC: Lan Segment: 1

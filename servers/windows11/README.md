# 📌 Visão Geral do Windows 11

Este diretório documenta a VM cliente Windows 11 utilizada no laboratório.
Este host consome os serviços disponibilizados pelos servidores do ambiente, com todo o tráfego controlado pelo Firewall (Fortigate).

## 🖥️ Configuração Geral da Máquina Cliente

Hostname: CLIENT-01

Sistema Operacional: Windows 11

### Serviços Utilizados

Active Directory (AD)

DNS

MySQL (acesso via cliente)

## 🌐 Configuração de Rede

IP: Automatic (DHCP)  
Gateway: Automatic (DHCP)  
Mask: Automatic (DHCP)  
Primary DNS: Automatic (DHCP)  
Alt DNS: Automatic (DHCP)

O DHCP é fornecido pelo Firewall, enquanto o DNS aponta para o Windows Server (AD/DNS).

## ⚙️ Configurações Iniciais Realizadas

Após a criação da VM cliente, foram executados os seguintes passos:

* Validação do funcionamento do DHCP do Firewall, confirmando a atribuição correta de IP, gateway e DNS.
* Ingresso da máquina no domínio infralab.local, previamente configurado no Windows Server.
* Verificação da política de Wallpaper

## 🗄️ Acesso ao MySQL Server

Para validação de conectividade com o servidor de banco de dados, foi instalado o MySQL Workbench na máquina cliente.

Parâmetros de Conexão Utilizados

Hostname: 192.168.0.3  
Port: 3306  
Username: gustavo  
Password: SenhaForte@123  

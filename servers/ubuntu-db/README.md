# 📌 Visão Geral do Ubuntu Server (MySQL)

Este diretório documenta a VM **Ubuntu Server** utilizada como **servidor dedicado de banco de dados MySQL** no laboratório.

O servidor fornece serviço de banco de dados para hosts da LAN, com acesso controlado pelo Firewall.

<br>

## 🖥️ Configuração Geral do Servidor

Hostname: srv-db  
Sistema Operacional: Ubuntu Server  
Função: MySQL Server (Dedicated)

<br>

## 🌐 Configuração de Rede

IP: 192.168.0.3  
Gateway: 192.168.0.1  
Mask: 255.255.255.0  
Primary DNS: 192.168.0.2

<br>

## 🗄️ Serviço MySQL

O MySQL foi instalado e configurado para atuar como serviço de banco de dados acessível remotamente.

### Características da Configuração

- MySQL rodando como serviço do sistema
- Usuário dedicado para acesso remoto (%)
- Database `projeto_db` criado para validação de conectividade

<br>

## 👤 Gerenciamento de Usuários

- O acesso inicial ao MySQL foi realizado via **root local**
- Um usuário dedicado foi criado para acesso remoto:

| User: gustavo  
| Password: SenhaForte@123  
| Plugin: mysql_native_password

<br>

## 🔐 Configuração De Acesso Remoto

Por padrão, o MySQL aceita conexões apenas de `localhost`.

Para permitir conexões externas:

- O parâmetro **bind-address** foi ajustado de 127.0.0.1 → 0.0.0.0 permitindo conexões remotas.
- O serviço MySQL foi reiniciado para aplicar as alterações

Com isso, o servidor passou a aceitar conexões vindas da VM cliente Windows.

<br>

## 🖥️ Integração com a VM Cliente

O acesso ao banco de dados foi validado a partir da VM **Windows 11 Client**, utilizando:

- MySQL Workbench

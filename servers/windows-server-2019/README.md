# 📌 Visão Geral do Windows Server

Este diretório documenta o servidor principal do ambiente, responsável por AD, DNS e GPOs e autenticação dos hosts. Este servidor integra todo o domínio e fornece os serviços essenciais de diretório, resolução de nomes e políticas centralizadas.

<br>

## 🖥️ Configuração Geral do Servidor

Hostname: SRV-DC  
Sistema Operacional: Windows Server 2019  

### Serviços:
Active Directory  
DNS Server

<br>

## 🌐 Configuração de Rede

IP: 192.168.0.2  
Gateway: 192.168.0.1  
Mask: 255.255.255.0  
Primary DNS: 192.168.0.2  
Alt DNS: 1.1.1.1

<br>

## 🧬 Active Directory

Domain: infralab.local  
Functional Level: Windows Server 2016

### 🔹 Estrutura Organizacional Ative Directory
```
Usuarios  
└── Setor  
      ├── Grupos
      |     └──<setor>-Admin
      |     └──<setor>-Pleno
      |     └──<setor>-Usuario
      |
      |
      |  
      └── Usuarios
```

<br>

## 🌐 DNS
Primary Zone: infralab.local  
Dynamic Update: Secure Only  
Foward Lookup Zone Type: Active Directory-Integrated

<br>

## 🎨 GPOs Implementadas
Wallpaper Corporativo

Caminho UNC:
```
\\SRV-DC\Users\Administrator\Pictures\Wallpapers\Wallpaper.png
```




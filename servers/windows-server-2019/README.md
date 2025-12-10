# 📌 Visão Geral do Windows Server

Este diretório documenta o servidor principal do ambiente, responsável por AD, DNS e GPOs e autenticação dos hosts. Este servidor integra todo o domínio e fornece os serviços essenciais de diretório, resolução de nomes e políticas centralizadas.

<br>

## 🖥️ Configuração Geral do Servidor

Hostname: SRV-DC  
Sistema Operacional: Windows Server 2019  
IP: 192.168.0.2

### Serviços:
Active Directory  
DNS Server

<br>

## 🧬 Active Directory

Domínio: infralab.local  
Nível funcional: Windows Server 2016

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



# 🔢 Comandos utilizados para configuração do Ubuntu Server / MySQL

1.  Atualização inicial do sistema

```
sudo apt update && sudo apt upgrade -y
```

2. Instalação do MySQL Server

```
sudo apt install mysql-server -y
```

3. Acesso ao MySQL usando o root

```
sudo su
mysql
```

4. Seleção do banco interno do MySQL

```
USE mysql;
```

5. Visualização dos usuários existentes atualmente

```
SELECT user, host, plugin FROM user;
```

6. Criação de usuário para não precisar usar o root e também acessar remotamente

```
CREATE USER 'gustavo'@'%' IDENTIFIED WITH mysql_native_password BY 'SenhaForte@123'
```

7. Ajuste para permitir conexões remotas, editando o arquivo "mysqld.cnf"

```
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

8. Alteração realizada:

```
bind address = 127.0.0.1 -> bind address: 0.0.0.0
```

9. Reinício do serviço MySQL para confirmar as alterações

```
sudo systemctl restart mysql
```

10. Servidor pronto para ser acessado pelo cliente.

# Manual - Backup e Restauração MySQL

Este guia demonstra como criar um dump (backup) e restaurar um banco de dados MySQL/MariaDB via linha de comando.

---

## 🔹 1. Criando um Backup (Dump)

Acesse a máquina onde o banco está instalado e execute:

```bash
mysqldump -u root <database> > <nome_do_arquivo_dump.sql>
````
- Se o usuário possuir senha:

```
mysqldump -u root -p <database> > <nome_do_arquivo_dump.sql>
```
#### Explicação dos parâmetros:

- mysqldump → ferramenta de exportação do MySQL

- u root → usuário do banco

- p → solicita senha

- wiki → nome do banco de dados

- \> → redireciona a saída para um arquivo

- backupwiki20260303.sql → nome do arquivo de backup

## 🔹 2. Restaurando um Backup

- Para restaurar o banco de dados:
  
> Se for maquina diferente envia o arquivo dump e siga os passos

OBS: O banco e o database tambem precisa esta criado e na maquina onde vai ser restaurado

# Manual de Instalação do MySQL Ubuntu 22.04

Este guia mostra como instalar o MySQL, criar um usuário.

---

## 🔹 3. Instale o banco se for preciso, pra isso tem outro manual. 

- Se for o caso va no manual depois volte nessa etapa. se ja tiver o banco siga os passos a baixo: 

## 🔹 4. Crie Databese:

```
create database <nome da base de dados>;
```

## 🔹 5. Criar usuário:

⚠️ Se a conexão for local mantenha no codigo o "localhost":
se for preciso conectar no workbench de outra maquina troque o "localhost" pelo IP da maquina que vai conectar ou coloque "%" isso lebera acesso de qualquer ip ou se for o caso de precisar liberar so para uma rede especifica voce vai trocar no codigo por exemplo rede 17 para liberar toda a rede 17 voce vai colocar assim "192.168.17.%".

No prompt do MySQL, execute:

```sql
CREATE USER 'usuario'@'localhost' IDENTIFIED BY 'senha desse usuario';
GRANT ALL PRIVILEGES ON *.* TO 'usuario'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```
# 🔹 6. Para restaurar o banco de dados:

- Saia do banco

```
exit
```

```
mysql -u root <database> > < <arquivo de backup.sql> -v
```

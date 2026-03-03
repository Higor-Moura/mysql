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

## 2. Restaurando um Backup

- Para restaurar o banco de dados:
  
> Se for maquina diferente envia o arquivo dump e siga os passos

OBS: O banco e o database tambem precisa esta criado e na maquina onde vai ser restaurado

```
mysql -u root <database> > < <arquivo de backup.sql>
```

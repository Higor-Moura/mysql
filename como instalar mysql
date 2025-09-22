# Manual de Instalação do MySQL e Configuração do Workbench no Ubuntu 22.04

Este guia mostra como instalar o MySQL, criar um usuário para o Workbench e configurar a conexão.

---

## 1. Atualizar repositórios

```bash
sudo apt update
```

## 2. Instalar o MySQL Server

```bash
sudo apt install mysql-server -y
```
⚠️ Se ocorrer o erro:
E: Dependências desencontradas. Tente 'apt --fix-broken install' sem nenhum pacote (ou especifique uma solução).

## 2.1 Corrigir pacotes quebrados

```bash 
sudo apt --fix-broken install
```

## 2.2 Atualizar repositórios novamente

```bash
sudo apt update
```

## 2.3 Instalar MySQL Server e Client corretamente

```bash
sudo apt install mysql-server mysql-client -y
```

## 3. Verificar status do serviço MySQL

```bash
systemctl status mysql
```
- Se o serviço estiver active (running), você já pode acessar o MySQL:

```bash
sudo mysql -u root
```

## 4. Criar usuário para o Workbench

No prompt do MySQL, execute:

```sql
CREATE USER 'master'@'localhost' IDENTIFIED BY '12345678';
GRANT ALL PRIVILEGES ON *.* TO 'master'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```
Sair do MySQL:

```sql
exit;
```

## 5. Testar login com o usuário criado

```bash
mysql -u master -p
```
Digite a senha: 12345678

## 6. Configurar no MySQL Workbench

- Host: 127.0.0.1

- Porta: 3306

- Usuário: master

- Senha: 12345678

Agora você está pronto para usar o MySQL Workbench.

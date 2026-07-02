# Guia de Instalação e Configuração do PostgreSQL (Debian)

Este documento descreve a instalação do PostgreSQL no Debian, ativação do serviço via systemd e configuração inicial de usuário e banco de dados.

---

## 1. Instalação

Atualize os pacotes:

```bash
sudo apt update && sudo apt upgrade -y
```
Instale o PostgreSQL:

```bash
sudo apt install postgresql postgresql-contrib -y
```

Verifique a versão instalada:

```bash
psql --version
```

1. Ativação do serviço (systemd)

Habilitar inicialização automática:

```bash
sudo systemctl enable postgresql
```

Iniciar o serviço:

```bash
sudo systemctl start postgresql
```

Verificar status:

```bash
systemctl status postgresql
```

Se aparecer active (running), o serviço está funcionando corretamente.

1. Acesso ao PostgreSQL (modo admin)

Entrar como usuário administrativo padrão:

```bash
sudo -u postgres psql
```
1. Criação de ROLE (usuário do banco)

Dentro do psql:

```sql
CREATE ROLE theus WITH LOGIN SUPERUSER CREATEDB CREATEROLE PASSWORD 'sua_senha_aqui';
```

Verificar roles existentes:

```sql
\du
```

1. Criação de DATABASE

Ainda dentro do psql:

```sql
CREATE DATABASE theus OWNER theus;
```

Listar bancos existentes:

```sql
\l
```

1. Teste de conexão

Saia do psql:

```sql
\q
```

Teste conexão:

```bash
psql -U theus -d theus
```
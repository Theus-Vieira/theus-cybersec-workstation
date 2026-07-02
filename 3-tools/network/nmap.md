# Nmap

## Objetivo

O Nmap (Network Mapper) é uma ferramenta para descoberta de hosts, varredura de portas, detecção de serviços, identificação de sistemas operacionais e auditoria de redes.

Este guia utiliza o pacote oficial do Debian.

---

# Método de instalação

Instalação utilizando o pacote oficial do Debian.

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y nmap
```

---

# Verificando a instalação

Confira a versão instalada:

```bash
nmap --version
```

Confira a localização do executável:

```bash
which nmap
```

Resultado esperado:

```text
/usr/bin/nmap
```

---

# Verificando o Nmap Scripting Engine (NSE)

Confira a localização dos scripts:

```bash
ls /usr/share/nmap/scripts
```

Atualize o banco de dados dos scripts:

```bash
sudo nmap --script-updatedb
```

---

# Atualizando

Mantenha o pacote atualizado:

```bash
sudo apt update
sudo apt upgrade
```

---

# Removendo

Remova o pacote:

```bash
sudo apt remove nmap
```

Para remover também arquivos de configuração:

```bash
sudo apt purge nmap
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/nmap
```

Scripts NSE:

```text
/usr/share/nmap/scripts
```

Banco de dados de serviços:

```text
/usr/share/nmap
```

Página de manual:

```text
/usr/share/man/man1/nmap.1.gz
```

---

# Comandos úteis

Versão:

```bash
nmap --version
```

Ajuda:

```bash
nmap --help
```

Atualizar banco de scripts:

```bash
sudo nmap --script-updatedb
```

Localizar o executável:

```bash
which nmap
```

Listar arquivos instalados pelo pacote:

```bash
dpkg -L nmap
```

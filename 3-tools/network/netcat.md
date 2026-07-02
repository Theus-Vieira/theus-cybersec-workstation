# Netcat (OpenBSD)

## Objetivo

O Netcat é uma ferramenta para leitura e escrita de dados através de conexões TCP e UDP.

É amplamente utilizada para testes de conectividade, transferência de arquivos, criação de listeners e depuração de serviços de rede.

Este guia utiliza a implementação OpenBSD, padrão do Debian.

---

# Método de instalação

Instalação utilizando o pacote oficial do Debian.

Pacote utilizado:

- netcat-openbsd

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y netcat-openbsd
```

---

# Verificando a instalação

Localize o executável:

```bash
which nc
```

Resultado esperado:

```text
/usr/bin/nc
```

Confira a versão:

```bash
nc -h
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
sudo apt remove netcat-openbsd
```

Para remover também arquivos de configuração:

```bash
sudo apt purge netcat-openbsd
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/nc
```

Página de manual:

```text
/usr/share/man/man1/nc.1.gz
```

---

# Comandos úteis

Ajuda:

```bash
nc -h
```

Localizar o executável:

```bash
which nc
```

Listar arquivos instalados:

```bash
dpkg -L netcat-openbsd
```

---

# Observações

O comando executável é:

```bash
nc
```

e não:

```bash
netcat
```

No Debian, o pacote `netcat-openbsd` fornece o executável `nc`.

Este guia documenta apenas a implementação OpenBSD.

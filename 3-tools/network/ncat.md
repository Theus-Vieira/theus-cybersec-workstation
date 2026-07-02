# Ncat

## Objetivo

O Ncat é uma ferramenta de comunicação e depuração de redes desenvolvida pelo projeto Nmap.

Ele suporta conexões TCP, UDP, IPv4, IPv6, SSL/TLS, proxies, redirecionamento de portas e diversas outras funcionalidades voltadas para administração de redes e testes de segurança.

No Debian 13 (Trixie), o Ncat é distribuído em um pacote independente.

---

# Método de instalação

Instalação utilizando o pacote oficial do Debian.

Pacote:

- ncat

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y ncat
```

---

# Verificando a instalação

Verifique a versão instalada:

```bash
ncat --version
```

Verifique a localização do executável:

```bash
which ncat
```

Resultado esperado:

```text
/usr/bin/ncat
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
sudo apt remove ncat
```

Para remover também os arquivos de configuração:

```bash
sudo apt purge ncat
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/ncat
```

Página de manual:

```text
/usr/share/man/man1/ncat.1.gz
```

---

# Comandos úteis

Versão:

```bash
ncat --version
```

Ajuda:

```bash
ncat --help
```

Manual:

```bash
man ncat
```

Localizar o executável:

```bash
which ncat
```

Listar os arquivos instalados pelo pacote:

```bash
dpkg -L ncat
```

Consultar informações do pacote:

```bash
apt show ncat
```

---

# Observações

O Ncat faz parte do projeto Nmap, porém, no Debian 13 (Trixie), ele é distribuído em um pacote separado.

O comando executável é:

```bash
ncat
```

Não confunda com o Netcat (OpenBSD), cujo executável é:

```bash
nc
```

Embora ambos tenham funcionalidades semelhantes, são ferramentas diferentes e possuem implementações distintas.

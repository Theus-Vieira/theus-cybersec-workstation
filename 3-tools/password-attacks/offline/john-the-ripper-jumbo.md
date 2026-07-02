# John the Ripper Jumbo

## Objetivo

O John the Ripper Jumbo é uma suíte para auditoria e recuperação de senhas.

A edição Jumbo adiciona suporte a centenas de formatos de hashes e arquivos protegidos, além de diversos utilitários auxiliares (john converters), tornando-se a versão recomendada para atividades de Pentest.

---

# Método de instalação

Instalação utilizando o repositório oficial do projeto.

# Pré-requisitos

Atualize os repositórios:

```bash
sudo apt update
```

Instale as dependências necessárias para compilação:

```bash
sudo apt install -y \
git \
build-essential \
pkg-config \
libssl-dev \
zlib1g-dev \
libbz2-dev \
liblzma-dev \
libgmp-dev \
libpcap-dev \
libkrb5-dev \
libopenmpi-dev \
yasm
```

---

# Criando o diretório de ferramentas

Caso ainda não exista:

```bash
sudo mkdir -p /opt/cybersec/tools
sudo chown -R $USER:$USER /opt/cybersec
```

---

# Clonando o repositório oficial

```bash
cd /opt/cybersec/tools

git clone git@github.com:openwall/john.git
```

Será criado:

```text
/opt/cybersec/tools/john
```

---

# Compilando

Entre no diretório de fontes:

```bash
cd /opt/cybersec/tools/john/src
```

Compile:

```bash
./configure
make -sj"$(nproc)"
```

---

# Verificando a compilação

Entre no diretório de execução:

```bash
cd ../run
```

Execute:

```bash
./john --list=build-info
```

---

# Adicionando ao PATH (Zsh)

Edite o arquivo:

```bash
nano ~/.zshrc
```

Adicione ao final:

```zsh
path+=("/opt/cybersec/tools/john/run")
```

# Criando um alias

Ainda no `~/.zshrc`, adicione:

```zsh
alias john="/opt/cybersec/tools/john/run/john"
```

Recarregue o shell:

```bash
source ~/.zshrc
```

---

# Verificando a instalação

Confira a versão:

```bash
john --list=build-info
```

Verifique a localização do executável:

```bash
which john
```

Resultado esperado:

```text
/opt/cybersec/tools/john/run/john
```

---

# Atualizando

Entre no diretório do projeto:

```bash
cd /opt/cybersec/tools/john
```

Atualize o código:

```bash
git pull
```

Recompile:

```bash
cd src

./configure
make -sj"$(nproc)"
```

---

# Removendo

Remova o diretório:

```bash
rm -rf /opt/cybersec/tools/john
```

Remova do `~/.zshrc`:

```zsh
path+=("/opt/cybersec/tools/john/run")

alias john="/opt/cybersec/tools/john/run/john"
```

Recarregue o shell:

```bash
source ~/.zshrc
```

---

# Diretórios utilizados

Código-fonte:

```text
/opt/cybersec/tools/john
```

Executável:

```text
/opt/cybersec/tools/john/run/john
```

Conversores:

```text
/opt/cybersec/tools/john/run/
```

---

# Ferramentas incluídas

Exemplos de utilitários disponíveis:

- ssh2john
- zip2john
- 7z2john
- rar2john
- pdf2john
- office2john
- keepass2john
- putty2john
- gpg2john
- dmg2john
- hccap2john
- racf2john
- pwsafe2john

---

# Comandos úteis

Versão:

```bash
john --list=build-info
```

Ajuda:

```bash
john --help
```

Listar formatos suportados:

```bash
john --list=formats
```

Listar conversores:

```bash
ls /opt/cybersec/tools/john/run/*2john*
```

---

# Observações

A edição Jumbo é a versão recomendada para laboratórios de Pentest, CTFs e auditorias de segurança, pois inclui centenas de formatos adicionais e diversos conversores que não estão presentes na edição Core.

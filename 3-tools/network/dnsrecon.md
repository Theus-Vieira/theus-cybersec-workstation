# DNSRecon

## Objetivo

O DNSRecon é uma ferramenta de reconhecimento DNS utilizada para enumeração de registros DNS, descoberta de subdomínios, transferências de zona, brute force e coleta de informações sobre domínios.

Este guia utiliza o **pipx**, método recomendado para instalar ferramentas Python em ambientes isolados.

---

# Método de instalação

Instalação utilizando o **pipx**.


# Pré-requisitos

Este guia pressupõe que o **pipx** já esteja instalado.

Verifique a instalação:

```bash
pipx --version
```

---

# Instalando

Execute:

```bash
pipx install dnsrecon
```

---

# Verificando a instalação

Confira a versão:

```bash
dnsrecon --version
```

Verifique a localização do executável:

```bash
which dnsrecon
```

Resultado esperado:

```text
/home/<usuario>/.local/bin/dnsrecon
```

---

# Atualizando

Atualize para a versão mais recente:

```bash
pipx upgrade dnsrecon
```

Confira novamente a versão:

```bash
dnsrecon --version
```

---

# Removendo

```bash
pipx uninstall dnsrecon
```

---

# Diretórios utilizados

Ambiente virtual:

```text
~/.local/share/pipx/venvs/dnsrecon
```

Executável:

```text
~/.local/bin/dnsrecon
```

---

# Comandos úteis

Versão:

```bash
dnsrecon --version
```

Ajuda:

```bash
dnsrecon --help
```

Localizar o executável:

```bash
which dnsrecon
```

Informações do ambiente pipx:

```bash
pipx list
```

---

# Observações

O pipx cria um ambiente virtual isolado para o DNSRecon, evitando conflitos de dependências com outras ferramentas Python instaladas no sistema.

Caso o diretório `~/.local/bin` ainda não esteja no `PATH`, adicione-o ao `~/.zshrc`:

```zsh
path+=("$HOME/.local/bin")
```

Recarregue o shell:

```bash
source ~/.zshrc
```

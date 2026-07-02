# pipx

## Objetivo

O pipx é um gerenciador para instalar e executar aplicações Python em ambientes isolados.

Ele é usado no cybersec-workstation para instalar ferramentas de segurança escritas em Python sem poluir o ambiente global do sistema.

Exemplos de ferramentas instaladas via pipx:

- dnsrecon
- mitmproxy
- evil-winrm (quando empacotado em Python)
- semgrep

---

# Método de instalação

No Debian 13 (Trixie), o pipx pode ser instalado via `apt`, pois é um utilitário do sistema e não uma ferramenta de pentest em si.

---

# Atualizando repositórios

```bash
sudo apt update
```

---

# Instalando pipx

```bash
sudo apt install -y pipx
```

---

# Inicializando o pipx no PATH

Após instalar, execute:

```bash
pipx ensurepath
```

Isso adiciona automaticamente o diretório de executáveis do pipx ao PATH do usuário.

---

# Para Zsh (configuração manual opcional)

Se necessário, adicione ao `~/.zshrc`:

```zsh
path+=("$HOME/.local/bin")
```

Recarregue o shell:

```bash
source ~/.zshrc
```

---

# Verificando a instalação

```bash
pipx --version
```

---

# Estrutura criada pelo pipx

O pipx organiza cada ferramenta em ambientes isolados:

```text
~/.local/share/pipx/venvs/
~/.local/bin/
```

---

# Instalando ferramentas com pipx

Formato padrão:

```bash
pipx install <pacote>
```

Exemplo:

```bash
pipx install dnsrecon
```

---

# Atualizando ferramentas

Atualizar um pacote específico:

```bash
pipx upgrade dnsrecon
```

Atualizar tudo:

```bash
pipx upgrade-all
```

---

# Removendo ferramentas

```bash
pipx uninstall dnsrecon
```

---

# Listando ferramentas instaladas

```bash
pipx list
```

---

# Reinstalar ferramenta (caso necessário)

```bash
pipx reinstall dnsrecon
```

---

# Diretórios utilizados

Executáveis:

```text
~/.local/bin/
```

Ambientes virtuais:

```text
~/.local/share/pipx/venvs/
```

Cache:

```text
~/.cache/pipx/
```

---

# Comandos úteis

Ver versão:

```bash
pipx --version
```

Garantir PATH:

```bash
pipx ensurepath
```

Listar ferramentas:

```bash
pipx list
```

---

# Observações

O pipx deve ser o padrão para instalação de ferramentas Python CLI no cybersec-workstation.

Evitar:

- pip install global
- sudo pip install

Sempre preferir pipx para ferramentas executáveis.
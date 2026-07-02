# Tor

## Objetivo

O Tor é uma rede de anonimização que protege a privacidade do usuário ao encaminhar o tráfego através de múltiplos nós distribuídos mundialmente.

Além do anonimato, o Tor permite o acesso a serviços Onion (.onion) e pode ser utilizado em ambientes de Pentest para roteamento de conexões através da rede Tor.

---

# Método de instalação

Instalação utilizando o repositório oficial do Tor Project.

Não utilizar:

- pacote padrão do Debian

---

# Pré-requisitos

Atualize os repositórios:

```bash
sudo apt update
```

Instale os pacotes necessários:

```bash
sudo apt install -y \
curl \
wget \
gnupg \
apt-transport-https \
lsb-release
```

---

# Verificando o codinome da distribuição

O Tor Project recomenda utilizar o codinome da distribuição instalada.

Verifique:

```bash
lsb_release -cs
```

Exemplo de saída:

```text
trixie
```

Guarde esse valor para o próximo passo.

---

# Adicionando a chave GPG

```bash
wget -qO- https://deb.torproject.org/torproject.org/A3C4F0F979CAA22CDBA8F512EE8CBC9E886DDD89.asc \
| gpg --dearmor \
| sudo tee /usr/share/keyrings/deb.torproject.org-keyring.gpg >/dev/null
```

---

# Adicionando o repositório oficial

Substitua `<DISTRIBUTION>` pelo resultado obtido com `lsb_release -cs`.

Exemplo para Debian 13 (Trixie):

```bash
echo "deb [signed-by=/usr/share/keyrings/deb.torproject.org-keyring.gpg] https://deb.torproject.org/torproject.org <DISTRIBUTION> main" \
| sudo tee /etc/apt/sources.list.d/tor.list
```

Opcionalmente, adicione também os pacotes fonte:

```bash
echo "deb-src [signed-by=/usr/share/keyrings/deb.torproject.org-keyring.gpg] https://deb.torproject.org/torproject.org <DISTRIBUTION> main" \
| sudo tee -a /etc/apt/sources.list.d/tor.list
```

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y \
tor \
torsocks \
deb.torproject.org-keyring
```

---

# Habilitando o serviço

```bash
sudo systemctl enable tor
sudo systemctl start tor
```

---

# Verificando a instalação

Versão:

```bash
tor --version
```

Status do serviço:

```bash
systemctl status tor
```

Verifique os executáveis:

```bash
which tor
which torsocks
which torify
```

Resultado esperado:

```text
/usr/bin/tor
/usr/bin/torsocks
/usr/bin/torify
```

---

# Ferramentas instaladas

A instalação disponibiliza:

- tor
- torsocks
- torify

**Observação:** o `torify` é um wrapper para o `torsocks` e permanece disponível por compatibilidade.

---

# Atualizando

```bash
sudo apt update
sudo apt upgrade
```

---

# Removendo

Remova os pacotes:

```bash
sudo apt remove \
tor \
torsocks \
deb.torproject.org-keyring
```

Remoção completa:

```bash
sudo apt purge \
tor \
torsocks \
deb.torproject.org-keyring
```

Remova também o repositório:

```bash
sudo rm /etc/apt/sources.list.d/tor.list
sudo rm /usr/share/keyrings/deb.torproject.org-keyring.gpg

sudo apt update
```

---

# Diretórios utilizados

Executáveis:

```text
/usr/bin/tor
/usr/bin/torsocks
/usr/bin/torify
```

Arquivo de configuração:

```text
/etc/tor/torrc
```

Dados do serviço:

```text
/var/lib/tor/
```

---

# Comandos úteis

Versão:

```bash
tor --version
```

Status do serviço:

```bash
systemctl status tor
```

Iniciar:

```bash
sudo systemctl start tor
```

Parar:

```bash
sudo systemctl stop tor
```

Reiniciar:

```bash
sudo systemctl restart tor
```

Executar um programa através da rede Tor:

```bash
torsocks <comando>
```

Exemplo:

```bash
torsocks curl https://check.torproject.org/api/ip
```

Compatibilidade com ferramentas antigas:

```bash
torify <comando>
```

---

# Observações

Este guia instala apenas o serviço Tor e suas ferramentas auxiliares.

O Tor Browser possui um método de instalação próprio e deve ser documentado separadamente.

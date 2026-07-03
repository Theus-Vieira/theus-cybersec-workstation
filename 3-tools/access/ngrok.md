# ngrok

## Objetivo

O ngrok é uma ferramenta de tunelamento seguro que permite expor serviços locais à Internet através de um túnel criptografado.

É muito utilizada em:

- Pentests
- Desenvolvimento Web
- APIs locais
- Webhooks
- Demonstrações
- Laboratórios

---

# Método de instalação

Instalação utilizando o repositório oficial do ngrok.

# Pré-requisitos

Atualize os repositórios:

```bash
sudo apt update
```

Instale as dependências:

```bash
sudo apt install -y \
curl \
gnupg2 \
ca-certificates
```

---

# Adicionando a chave GPG

```bash
curl -fsSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
| sudo gpg --dearmor -o /usr/share/keyrings/ngrok.gpg
```

---

# Adicionando o repositório oficial

```bash
echo "deb [signed-by=/usr/share/keyrings/ngrok.gpg] https://ngrok-agent.s3.amazonaws.com bookworm main" \
| sudo tee /etc/apt/sources.list.d/ngrok.list
```

> **Observação:** caso o ngrok passe a disponibilizar um repositório específico para o Debian 13 (Trixie), substitua `bookworm` pelo codinome recomendado na documentação oficial.

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y ngrok
```

---

# Verificando a instalação

Versão:

```bash
ngrok version
```

Executável:

```bash
which ngrok
```

Resultado esperado:

```text
/usr/bin/ngrok
```

---

# Criando uma conta

Acesse:

https://dashboard.ngrok.com/signup

Após criar sua conta, faça login no Dashboard.

---

# Obtendo o Authtoken

No Dashboard:

**Your Authtoken**

Copie o token fornecido.

---

# Configurando o Authtoken

Execute:

```bash
ngrok config add-authtoken <SEU_AUTHTOKEN>
```

Exemplo:

```bash
ngrok config add-authtoken 2AbCdEfGhIjKlMnOpQrStUvWxYz123456789
```

---

# Verificando a configuração

Arquivo de configuração:

```text
~/.config/ngrok/ngrok.yml
```

Consultar a configuração:

```bash
ngrok config check
```

---

# Atualizando

```bash
sudo apt update
sudo apt upgrade
```

---

# Removendo

```bash
sudo apt remove ngrok
```

Remoção completa:

```bash
sudo apt purge ngrok
```

Remover o repositório:

```bash
sudo rm /etc/apt/sources.list.d/ngrok.list
sudo rm /usr/share/keyrings/ngrok.gpg

sudo apt update
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/ngrok
```

Configuração:

```text
~/.config/ngrok/ngrok.yml
```

---

# Comandos úteis

Versão:

```bash
ngrok version
```

Ajuda:

```bash
ngrok help
```

Verificar configuração:

```bash
ngrok config check
```

Abrir um túnel HTTP na porta 8080:

```bash
ngrok http 8080
```

Abrir um túnel TCP para SSH:

```bash
ngrok tcp 22
```

---

# Observações

- É necessário possuir uma conta no ngrok.
- O Authtoken é obrigatório para utilizar os recursos completos da ferramenta.
- O plano gratuito possui limitações de conexões, domínios e tempo de uso.

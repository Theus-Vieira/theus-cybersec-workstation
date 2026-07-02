# Wireshark

## Objetivo

O Wireshark é um analisador de protocolos de rede utilizado para captura e inspeção de tráfego em tempo real.

Ele permite análise detalhada de pacotes TCP/IP, DNS, HTTP, TLS e diversos outros protocolos.

---

# Método de instalação

Instalação utilizando o pacote oficial do Debian.

---

# Atualizando repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y wireshark
```

Durante a instalação, o sistema pode perguntar:

```text
Should non-superusers be able to capture packets?
```

Recomendado:

- selecionar **Yes**

---

# Adicionando usuário ao grupo wireshark

Para permitir captura sem root:

```bash
sudo usermod -aG wireshark $USER
```

Depois faça logout/login.

---

# Verificando a instalação

```bash
wireshark --version
```

Verificar executável:

```bash
which wireshark
```

---

# Iniciando captura via terminal

```bash
wireshark
```

Ou via terminal leve:

```bash
tshark --version
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
sudo apt remove wireshark
```

Remoção completa:

```bash
sudo apt purge wireshark
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/wireshark
```

TShark:

```text
/usr/bin/tshark
```

Plugins:

```text
/usr/lib/x86_64-linux-gnu/wireshark/
```

Configuração do usuário:

```text
~/.config/wireshark/
```

---

# Comandos úteis

Versão:

```bash
wireshark --version
```

TShark versão:

```bash
tshark --version
```

Listar interfaces:

```bash
tshark -D
```

Captura básica:

```bash
tshark -i eth0
```

---

# Observações

O Wireshark possui dois componentes principais:

- **wireshark** → interface gráfica
- **tshark** → versão em linha de comando

Ambos são instalados pelo mesmo pacote no Debian.

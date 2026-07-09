# OpenVPN

## Objetivo

O OpenVPN é uma solução de VPN (Virtual Private Network) que permite estabelecer conexões seguras entre o computador e redes remotas utilizando criptografia TLS.

Na área de Pentest é amplamente utilizado para conectar-se a laboratórios como:

- Hack The Box
- TryHackMe
- VulnHub
- Ambientes corporativos
- Infraestruturas de clientes

---

# Método de instalação

Instalação utilizando os pacotes oficiais do Debian.

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y \
openvpn \
resolvconf
```

> O pacote `resolvconf` é recomendado para atualização automática do DNS durante o estabelecimento da VPN.

---

# Verificando a instalação

Versão:

```bash
openvpn --version
```

Executável:

```bash
which openvpn
```

Resultado esperado:

```text
/usr/sbin/openvpn
```

---

# Testando a instalação

Exibir ajuda:

```bash
openvpn --help
```

---

# Utilizando um arquivo .ovpn

Conecte-se utilizando um perfil fornecido pelo laboratório ou cliente:

```bash
sudo openvpn --config caminho/para/arquivo.ovpn
```

Exemplo:

```bash
sudo openvpn --config ~/VPN/htb.ovpn
```

---

# Encerrando a conexão

Pressione:

```text
CTRL + C
```

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
sudo apt remove openvpn resolvconf
```

Remoção completa:

```bash
sudo apt purge openvpn resolvconf
```

---

# Diretórios utilizados

Executável:

```text
/usr/sbin/openvpn
```

Configuração global:

```text
/etc/openvpn/
```

Configurações do cliente:

```text
/etc/openvpn/client/
```

Configurações do servidor:

```text
/etc/openvpn/server/
```

Logs (quando configurados):

```text
/var/log/openvpn/
```

---

# Comandos úteis

Versão:

```bash
openvpn --version
```

Ajuda:

```bash
openvpn --help
```

Executar um perfil:

```bash
sudo openvpn --config arquivo.ovpn
```

Ver interfaces VPN:

```bash
ip addr
```

Ver rotas:

```bash
ip route
```

---

# Observações

Este guia instala apenas o cliente OpenVPN.

Os arquivos de configuração (`.ovpn`) normalmente são fornecidos pela plataforma ou pela organização responsável pela VPN.

Após estabelecer a conexão, recomenda-se verificar:

- endereço IP atribuído;
- rotas adicionadas;
- servidores DNS;
- conectividade com a rede remota.

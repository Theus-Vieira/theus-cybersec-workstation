# Burp Suite Community Edition

## Objetivo

O Burp Suite Community Edition é uma plataforma para testes manuais de segurança em aplicações Web desenvolvida pela PortSwigger.

Este pass-a-passo utiliza exclusivamente o instalador oficial da PortSwigger, garantindo que a versão instalada seja a mais recente disponível.

## Instalação

### Pré-requisitos

Java não é necessário.

As versões atuais do Burp Suite já incluem o runtime necessário durante a instalação.

---

### Baixando o instalador

Entre no diretório de downloads:

```bash
cd ~/Downloads
```

Baixe a versão Linux x64 (para a pasta Downloads) diretamente da página oficial:

[Página Oficial](https://portswigger.net/burp/downloads)

O arquivo será semelhante a:

```text
burpsuite_linux_v2026.4.3.sh
```

> O nome do arquivo muda a cada nova versão.

---

### Tornando o instalador executável

```bash
chmod +x burpsuite_linux_v*.sh
```

---

### Executando a instalação

```bash
sudo ./burpsuite_linux_v*.sh
```

---

### Verificando a instalação

Execute:

```bash
burpsuite
```

Caso o comando não exista:

```bash
which burpsuite
```

ou

```bash
find /opt -name burpsuite -type f 2>/dev/null
```

---

### Configurando o PATH (Zsh)

Se o executável não estiver no PATH, descubra onde ele foi instalado:

```bash
find /opt -type f -name burpsuite 2>/dev/null
```

Exemplo:

```text
/opt/BurpSuiteCommunity/burpsuite
```

Adicione o diretório ao `~/.zshrc`:

```zsh
# Burp Suite
path+=("/opt/BurpSuiteCommunity")
```

Recarregue o shell:

```bash
source ~/.zshrc
```

---

## Atualizando

A atualização é feita instalando novamente a versão mais recente obtida na página oficial.

O instalador migra automaticamente as configurações da versão anterior.

---

## Removendo

Caso tenha sido instalado em:

```text
/opt/BurpSuiteCommunity
```

Remova:

```bash
sudo rm -rf /opt/BurpSuiteCommunity
```

Remova também a entrada correspondente do `~/.zshrc`, caso tenha sido adicionada manualmente.

---

## Diretórios utilizados

Instalação:

```text
/opt/BurpSuiteCommunity
```

Configurações do usuário:

```text
~/.BurpSuite
```

---

## Comandos úteis

Executar:

```bash
burpsuite
```

Localizar o executável:

```bash
which burpsuite
```

Encontrar a instalação:

```bash
find /opt -name burpsuite
```

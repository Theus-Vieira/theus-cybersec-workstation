# DirB

## Objetivo

O DirB é uma ferramenta de brute force para descoberta de diretórios e arquivos em servidores web utilizando listas de palavras (wordlists).

Como o projeto original não possui mais um repositório oficial mantido e seu desenvolvimento encontra-se descontinuado, este guia utiliza o pacote mantido pela equipe do Debian.

Lembrando que essa ferramenta já foi superada por ferramentas mais modernas como gobuster, ffuf e outras mais.

---

# Método de instalação

Instalação utilizando o pacote oficial do Debian.

---

# Atualizando os repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install dirb
```

---

# Verificando a instalação

Confira a localização do executável:

```bash
which dirb
```

Confira a ajuda da ferramenta:

```bash
dirb
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

```bash
sudo apt remove dirb
```

Para remover também os arquivos de configuração:

```bash
sudo apt purge dirb
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/dirb
```

Wordlists:

```text
/usr/share/dirb/
```

---

# Comandos úteis

Executar:

```bash
dirb
```

Localizar o executável:

```bash
which dirb
```

Listar os arquivos instalados pelo pacote:

```bash
dpkg -L dirb
```

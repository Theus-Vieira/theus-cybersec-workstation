# Foremost

## Objetivo

O Foremost é uma ferramenta de recuperação de arquivos (file carving) utilizada para extrair arquivos de imagens de disco, dispositivos de armazenamento e outros arquivos binários, com base em suas assinaturas (headers e footers).

É amplamente utilizada em atividades de perícia computacional (Digital Forensics) e resposta a incidentes.

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
sudo apt install -y foremost
```

---

# Verificando a instalação

Verifique a versão instalada:

```bash
foremost -V
```

Verifique a localização do executável:

```bash
which foremost
```

Resultado esperado:

```text
/usr/bin/foremost
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
sudo apt remove foremost
```

Para remover também arquivos de configuração:

```bash
sudo apt purge foremost
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/foremost
```

Arquivo de configuração:

```text
/etc/foremost.conf
```

Página de manual:

```text
/usr/share/man/man8/foremost.8.gz
```

---

# Comandos úteis

Ver versão:

```bash
foremost -V
```

Exibir ajuda:

```bash
foremost -h
```

Consultar o manual:

```bash
man foremost
```

Localizar o executável:

```bash
which foremost
```

Listar os arquivos instalados pelo pacote:

```bash
dpkg -L foremost
```

---

# Observações

O Foremost utiliza um arquivo de configuração para definir os tipos de arquivos que podem ser recuperados:

```text
/etc/foremost.conf
```

As alterações nesse arquivo afetam o comportamento da ferramenta durante a recuperação de arquivos.

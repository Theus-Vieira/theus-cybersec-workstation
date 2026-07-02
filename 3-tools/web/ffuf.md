# ffuf

## Objetivo

O ffuf (Fuzz Faster U Fool) é uma ferramenta de fuzzing para aplicações web, utilizada principalmente para descoberta de diretórios, arquivos, subdomínios, parâmetros e Virtual Hosts.

Este passo-a-passo utiliza o método oficial recomendado pelos desenvolvedores, instalando o ffuf diretamente pelo Go.

---

# Pré-requisitos

Este guia pressupõe que o Go já esteja instalado.

Verifique a instalação:

```bash
go version
```

---

# Instalando

Execute:

```bash
go install github.com/ffuf/ffuf/v2@latest
```

O executável será instalado em:

```text
~/go/bin
```

Como o diretório já foi adicionado ao PATH durante a instalação do Go, o comando ficará disponível automaticamente.

---

# Verificando a instalação

Confira a versão:

```bash
ffuf -V
```

ou

```bash
ffuf --version
```

Confira também a localização do executável:

```bash
which ffuf
```

Resultado esperado:

```text
/home/<usuario>/go/bin/ffuf
```

---

# Atualizando

Atualize para a versão mais recente:

```bash
go install github.com/ffuf/ffuf/v2@latest
```

Verifique novamente:

```bash
ffuf -V
```

---

# Removendo

Localize o executável:

```bash
which ffuf
```

Remova:

```bash
rm "$(which ffuf)"
```

---

# Diretórios utilizados

Executável:

```text
~/go/bin/ffuf
```

Workspace Go:

```text
~/go
```

Cache de módulos:

```text
~/go/pkg/mod
```

---

# Comandos úteis

Versão:

```bash
ffuf -V
```

Ajuda:

```bash
ffuf -h
```

Localizar o executável:

```bash
which ffuf
```

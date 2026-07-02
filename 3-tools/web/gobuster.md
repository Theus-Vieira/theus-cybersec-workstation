# Gobuster

## Objetivo

O Gobuster é uma ferramenta escrita em Go para enumeração de diretórios, arquivos, subdomínios, Virtual Hosts, buckets S3 e buckets GCS.

Este guia utiliza o método oficial recomendado pelos desenvolvedores, instalando o Gobuster diretamente pelo Go.

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
go install github.com/OJ/gobuster/v3@latest
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
gobuster version
```

Confira também a localização do executável:

```bash
which gobuster
```

Resultado esperado:

```text
/home/<usuario>/go/bin/gobuster
```

---

# Atualizando

Atualize para a versão mais recente:

```bash
go install github.com/OJ/gobuster/v3@latest
```

Verifique novamente:

```bash
gobuster version
```

---

# Removendo

Localize o executável:

```bash
which gobuster
```

Remova:

```bash
rm "$(which gobuster)"
```

---

# Diretórios utilizados

Executável:

```text
~/go/bin/gobuster
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
gobuster version
```

Ajuda:

```bash
gobuster --help
```

Listar módulos disponíveis:

```bash
gobuster --help
```

Localizar o executável:

```bash
which gobuster
```

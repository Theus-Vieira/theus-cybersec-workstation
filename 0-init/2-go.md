# GO

Primeira coisa a se responder é: por quê instalar o GO?

Bom muitas ferramentas novas são escritas nesta linguagem e podemos instalar com o GO. Com isso teremos acesso a ferramentas atualizadas.

## Instalação

Primeiro precisamos pegar a versão mais atualizada do go em 

[Site Oficial](https://go.dev/dl/)

ou tu baixa direto do site, ou copia a url de download da ferramenta. 

---

# Baixando o Go

Entre no diretório de downloads:

```bash
cd ~/Downloads
```

Baixe o arquivo, se não baixou pelo link direto:

```bash
wget https://go.dev/dl/go1.26.4.linux-amd64.tar.gz
```

---

# Removendo instalações anteriores

Caso exista uma instalação manual antiga:

```bash
sudo rm -rf /usr/local/go
```

> Este comando não remove projetos Go nem o diretório `~/go`.

---

# Instalando

Extraia o pacote em `/usr/local`:

```bash
sudo tar -C /usr/local -xzf go1.26.4.linux-amd64.tar.gz
```

---

# Configurando o PATH

Edite o arquivo:

```bash
nano ~/.zshrc
```

Adicione ao final:

```bash
# Go

typeset -U path PATH # Se já tiver essa linha, não precisa duplicar.

path+=('/usr/local/go/bin:$PATH')
path+=('$PATH:$HOME/go/bin')

```

Salve o arquivo e recarregue o shell:

```bash
source ~/.zshrc
```

---

# Verificando a instalação

Confira a versão instalada:

```bash
go version
```

Resultado esperado:

```text
go version go1.26.4 linux/amd64
```

Verifique também o ambiente:

```bash
go env
```

---

# Instalando ferramentas

O método oficial para instalar ferramentas escritas em Go é:

```bash
go install <módulo>@latest
```

### Exemplo

Instalando o `httpx`:

```bash
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
```

Após a instalação:

```bash
httpx -version
```

O executável será instalado em:

```text
~/go/bin
```

---

# Atualizando uma ferramenta

Execute novamente:

```bash
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
```

---

# Removendo uma ferramenta

Descubra onde ela está instalada:

```bash
which httpx
```

Remova o executável:

```bash
rm "$(which httpx)"
```

---

# Diretórios utilizados

Instalação do Go:

```text
/usr/local/go
```

Executáveis instalados com `go install`:

```text
~/go/bin
```

Cache de módulos:

```text
~/go/pkg/mod
```

Workspace padrão:

```text
~/go
```

---

# Comandos úteis

Versão do Go:

```bash
go version
```

Informações do ambiente:

```bash
go env
```

Local do workspace:

```bash
go env GOPATH
```

Local dos binários:

```bash
go env GOBIN
```
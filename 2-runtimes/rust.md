# Rust

## Objetivo

Rust é uma linguagem de programação de sistemas focada em desempenho e segurança. Diversas ferramentas modernas de Segurança da Informação são desenvolvidas em Rust e distribuídas através do Cargo, o gerenciador oficial de pacotes da linguagem.

Exemplos de ferramentas escritas em Rust:

- feroxbuster
- ripgen
- x8
- trufflehog
- sniffnet

---

# Método de instalação

Este passo-a-passo utiliza o método oficial recomendado pelo projeto Rust, através do instalador `rustup`.

---

# Instalando o Rust

Baixe e execute o instalador oficial:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Quando o instalador perguntar qual opção deseja utilizar, selecione:

```text
1) Proceed with standard installation (default)
```

A instalação criará:

```text
~/.cargo
```

---

# Configurando o PATH (Zsh)

Edite o arquivo:

```bash
nano ~/.zshrc
```

Adicione ao final:

```zsh
# Rust
path+=("$HOME/.cargo/bin")
```

Recarregue o shell:

```bash
source ~/.zshrc
```

---

# Verificando a instalação

Confira a versão do compilador:

```bash
rustc --version
```

Confira a versão do Cargo:

```bash
cargo --version
```

Verifique também o Rustup:

```bash
rustup --version
```

---

# Atualizando o Rust

Atualize todos os componentes instalados:

```bash
rustup update
```

Verifique novamente:

```bash
rustc --version
```

---

# Instalando ferramentas

O método oficial para instalar ferramentas em Rust é:

```bash
cargo install <nome-da-ferramenta>
```

### Exemplo

Instalando o ripgen:

```bash
cargo install ripgen
```

Após a instalação:

```bash
ripgen --help
```

Os executáveis serão instalados em:

```text
~/.cargo/bin
```

---

# Atualizando uma ferramenta

```bash
cargo install ripgen --force
```

---

# Removendo uma ferramenta

```bash
cargo uninstall ripgen
```

---

# Atualizando todas as ferramentas

O Cargo não possui um comando nativo para atualizar todas as ferramentas instaladas.

Para isso, instale o utilitário oficial da comunidade:

```bash
cargo install cargo-update
```

Depois utilize:

```bash
cargo install-update -a
```

---

# Diretórios utilizados

Instalação do Rust:

```text
~/.rustup
```

Cargo:

```text
~/.cargo
```

Executáveis:

```text
~/.cargo/bin
```

Registro de crates:

```text
~/.cargo/registry
```

Git cache:

```text
~/.cargo/git
```

---

# Comandos úteis

Versão do compilador:

```bash
rustc --version
```

Versão do Cargo:

```bash
cargo --version
```

Versão do Rustup:

```bash
rustup --version
```

Atualizar Rust:

```bash
rustup update
```

Listar toolchains instaladas:

```bash
rustup toolchain list
```

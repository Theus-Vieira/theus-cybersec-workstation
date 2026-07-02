# sqlmap

## Objetivo

O sqlmap é uma ferramenta open source para detecção e exploração automatizada de vulnerabilidades de SQL Injection.

Este guia utiliza o repositório oficial do projeto, garantindo uma instalação sempre atualizada e de fácil manutenção.

---

# Pré-requisitos

Verifique se o Git está instalado:

```bash
git --version
```

Verifique a versão do Python:

```bash
python3 --version
```

---

# Criando o diretório de ferramentas

Caso ainda não exista:

```bash
sudo mkdir -p /opt/cybersec/tools
```

Conceda a propriedade ao seu usuário:

```bash
sudo chown -R $USER:$USER /opt/cybersec
```

---

# Clonando o repositório oficial

Entre no diretório:

```bash
cd /opt/cybersec/tools
```

Clone o projeto:

```bash
git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git
```

Será criado:

```text
/opt/cybersec/tools/sqlmap
```

---

# Criando um link simbólico

Crie um link para facilitar a execução:

```bash
sudo ln -sf /opt/cybersec/tools/sqlmap/sqlmap.py /usr/local/bin/sqlmap
```

Torne o script executável:

```bash
chmod +x /opt/cybersec/tools/sqlmap/sqlmap.py
```

---

# Verificando a instalação

Execute:

```bash
sqlmap --version
```

ou

```bash
python3 /opt/cybersec/tools/sqlmap/sqlmap.py --version
```

O sqlmap exibirá a versão instalada.

---

# Atualizando

Entre no diretório da ferramenta:

```bash
cd /opt/cybersec/tools/sqlmap
```

Atualize:

```bash
git pull
```

Verifique novamente:

```bash
sqlmap --version
```

---

# Removendo

Remova o link simbólico:

```bash
sudo rm /usr/local/bin/sqlmap
```

Remova o diretório:

```bash
rm -rf /opt/cybersec/tools/sqlmap
```

---

# Diretórios utilizados

Instalação:

```text
/opt/cybersec/tools/sqlmap
```

Executável:

```text
/usr/local/bin/sqlmap
```

---

# Comandos úteis

Versão:

```bash
sqlmap --version
```

Atualizar:

```bash
git pull
```

Localizar o executável:

```bash
which sqlmap
```

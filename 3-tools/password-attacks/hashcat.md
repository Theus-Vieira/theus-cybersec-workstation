# Hashcat

## Objetivo

O Hashcat é uma ferramenta de recuperação de senhas baseada em GPU/CPU, utilizada para cracking de hashes com suporte a múltiplos algoritmos e modos de ataque.

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
sudo apt install -y hashcat
```

---

# Verificando a instalação

```bash
hashcat --version
```

Verificar ajuda:

```bash
hashcat -h
```

Localizar executável:

```bash
which hashcat
```

---

# Testando suporte a GPU/CPU

Listar dispositivos disponíveis:

```bash
hashcat -I
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
sudo apt remove hashcat
```

Remoção completa:

```bash
sudo apt purge hashcat
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/hashcat
```

Regras:

```text
/usr/share/hashcat/rules/
```

Dicionários e exemplos:

```text
/usr/share/hashcat/
```

---

# Comandos úteis

Versão:

```bash
hashcat --version
```

Listar modos de hash:

```bash
hashcat --help
```

Detectar hardware:

```bash
hashcat -I
```

Executar benchmark:

```bash
hashcat -b
```

---

# Observações

- Hashcat depende fortemente de drivers de GPU para desempenho ideal.
- Em sistemas com NVIDIA/AMD, drivers corretos são essenciais.
- CPU mode funciona, mas é significativamente mais lento.


# Hydra (THC-Hydra)

## Objetivo

O Hydra é uma ferramenta de ataque de força bruta e password guessing utilizada para testar autenticação em serviços de rede.

Ele suporta múltiplos protocolos e é amplamente usado em testes de segurança para validação de credenciais fracas ou reutilizadas.

---

# Método de instalação

Instalação utilizando o pacote oficial do Debian.

No Debian 13 (Trixie), o Hydra está disponível nos repositórios oficiais e possui versão suficientemente atual para uso em 2026.

---

# Atualizando repositórios

```bash
sudo apt update
```

---

# Instalando

```bash
sudo apt install -y hydra
```

---

# Verificando a instalação

Verificar versão:

```bash
hydra -v
```

Verificar ajuda:

```bash
hydra -h
```

Localizar executável:

```bash
which hydra
```

Resultado esperado:

```text
/usr/bin/hydra
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
sudo apt remove hydra
```

Remoção completa:

```bash
sudo apt purge hydra
```

---

# Diretórios utilizados

Executável:

```text
/usr/bin/hydra
```

Wordlists (dependendo do sistema):

```text
/usr/share/wordlists/
```

Módulos de serviços:

```text
/usr/share/hydra/
```

---

# Comandos úteis

Ajuda geral:

```bash
hydra -h
```

Exibir módulos suportados:

```bash
hydra -U
```

Exemplo de teste de sintaxe (sem ataque real):

```bash
hydra -h | head
```

---

# Observações

- O Hydra realiza ataques **online**, ou seja, contra serviços em execução.
- O desempenho depende diretamente da latência da rede e da taxa de bloqueio do alvo.
- Pode gerar logs em sistemas de defesa (IDS/IPS).

---

# Boas práticas

- Evitar uso em serviços sem autorização explícita.
- Preferir ambientes controlados (labs, CTFs, máquinas virtuais).
- Ajustar limites de threads para evitar bloqueios prematuros.

---

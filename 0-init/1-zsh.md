# ZSH

Aqui entramos em uma questão de preferência...

ZSH é um shell e eu estou colocando ela aqui pua e simplesmente porque eu gosto dele por uma questão de personalização e produtividade.

O Debian vem com o bash instalado e tá tudo certo, se não quiser isntalar o zsh, pula essa etapa.

Só fique atento pra quando em uma instalação eu disser reinicie o seu terminal com ```source ~/.zshrc```, execute ```source ~/.bashrc``` se estiver usando o bash, beleza?

Ah, e também no .zshrc eu termino usando uma sintaxe diferente ao adicionar algo a path. Esse método é exclusivo do zsh e ele impede de haver duplicatas no path

```zsh
typeset -U path PATH

path+=('/opt/cybersec/tools/john/run')
```

Se você usa bash, você fará:


```bash

export PATH="/opt/cybersec/tools/john/run:$PATH"
```

## Instalação do zsh

```shell
sudo apt update
sudo apt install -y zsh zsh-syntax-highlighting zsh-autosuggestions

chsh -s /bin/zsh "$USER"
```

O que esse comando faz é atualizar a lista de pacotes, instalar o zsh, highlihts e sugestions e por fim selecionar o sh como a sua shell principal.

Depois disso, deve-se encerrar a sessão e logar novamente ou reiniciar o sistema.
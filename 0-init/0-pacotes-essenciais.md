# Pacotes Essenciais

Antes de começar a instalação das ferramentas propriamente ditas, vamos nos certificar de instalar os pacotes necessários para o funcionamento delas.

[!] Antes de instalar, sugiro que olhe o que está sendo instalado. Eu sei que são pacotes e tudo, mas observem e pesquisem sobre os eles. Isso é importante

```
sudo apt install -y \
build-essential \
git \
curl \
wget \
unzip \
zip \
tar \
gzip \
bzip2 \
xz-utils \
make \
cmake \
pkg-config \
ca-certificates \
gnupg \
lsb-release \
software-properties-common \
apt-transport-https \
jq \
yq \
tree \
vim \
nano \
tmux \
screen \
ripgrep \
fd-find \
fzf \
bat \
eza \
htop \
btop \
ncdu \
lsof \
strace \
ltrace \
file \
binutils \
dnsutils \
whois \
net-tools \
iproute2 \
iputils-ping \
traceroute \
tcpdump \
tshark \
openssh-client \
openssl
```

Caso fique dando erro de policykit que é aquele popup que aparece para colocar a senha quando entra em algum app, instala-se o pacote para isso:

```bash
sudo apt install lxpolkit -y
```

E se estiver no gnome e quiser personalizar o dock de apps:

```bash
sudo apt install gnome-shell-extension-dashtodock -y
```

# Configurações do Meu Setup

Abaixo as configurações do pc

```
theus@CyberSec
--------------
OS: Debian GNU/Linux 13 (trixie) x86_64
Host: Inspiron 3537 (A08)
Kernel: Linux 6.12.95+deb13-amd64
Uptime:
Packages:
Shell: zsh 5.9
Display (eDP-1):
WM: i3 (X11)
Cursor: 
Terminal:
Terminal Font:
CPU: Intel(R) Core(TM) i7-4500U (4) @ 3.00 GHz
GPU 1: AMD Radeon HD 8850M / R9 M265X
GPU 2: Intel Haswell-ULT Integrated Graphics Controller @ 1.10 GHz [Integrated]
Memory: 2.08 GiB / 15.52 GiB (13%)
Swap: 0 B / 15.90 GiB (0%)
Disk (/): 86.07 GiB / 422.45 GiB (20%) - ext4
Local IP (wlp2s0):
Locale:
```

Neste setup específico eu tenho uma gpu híbrida e elas estão competindo entre si. Então o que eu tenho que fazer é desativar a problemática que nesse caso é a radeon editando o arquivo ```/etc/default/grub```, buscando a linha que contém ```GRUB_CMDLINE_LINUX_DEFAULT=""``` e adicionando entre as aspas ```modprobe.blacklist=radeon,amdgpu```

Depois é só atualizar o grub e o iniciador com:

```bash
sudo update-initramfs -u -k all && sudo update-grub
```


# Linuxmint_qcow2

(Türkçe🇹🇷)
### Ön Gereksinimler (Termux)
Bu projeyi Termux üzerinde çalıştırmak için aşağıdaki paketleri kurmanız gerekir:

1. **QEMU'yu kur ve güncelle:**
   pkg update && pkg install qemu-utils qemu-common qemu-system-x86-64-headless

2. **VNC Viewer:**
   Play Store'dan bir VNC Viewer uygulaması indirin (örneğin: RealVNC).

### Kurulum

1. **Dosyaları birleştir:**
   cat linuxmint_part00.zip linuxmint_part01.zip linuxmint_part02.zip > linuxmint_qcow2.zip

2. **Sanal Makineyi çalıştır:**
   qemu-system-x86_64 -m 4096 -smp 4 -drive file=mint_disk.qcow2,format=qcow2 -net nic -net user -vnc :0

3. **VNC'ye bağlan:**
   VNC Viewer uygulamanızı açın ve localhost:5900 ya da 127.0.0.1:5900 adresine bağlanın.

*Not: -m değeri RAM kullanım miktarını, -smp değeri ise kaç çekirdek kullanılacağını belirtir.*


(English)
### Prerequisites (Termux)
To run this project on Termux, you need to install the following packages:

1. **Install and Update QEMU:**
   pkg update && pkg install qemu-utils qemu-common qemu-system-x86-64-headless

2. **VNC Client:**
   Install a VNC Viewer app from the Play Store (e.g.: RealVNC).

### Setup

1. **Merge files:**
   cat linuxmint_part00.zip linuxmint_part01.zip linuxmint_part02.zip > linuxmint_qcow2.zip

2. **Run the VM:**
   qemu-system-x86_64 -m 4096 -smp 4 -drive file=mint_disk.qcow2,format=qcow2 -net nic -net user -vnc :0

3. **Connect to VNC:**
   Open your VNC Viewer app and connect to:
   localhost:5900 or 127.0.0.1:5900

*Note: -m value = how much ram using, -smp value = how many cores using.*

# Linux QEMU

This repository stores note on using qemu on linux.

## Disk

Creating a new disk image:  
```bash
qemu-img create -f qcow2 u24.img 25G
```

Resizing a disk image:  
```bash
qemu-img resize u24.img +30G
```

## x86_64

Booting with an image:  
```bash
qemu-system-x86_64 -enable-kvm -cdrom /home/chanjl/Downloads/ubuntu-24.04.2-desktop-amd64.iso -boot menu=on -drive file=$HOME/reference/qemu_images/u24.img -m 6G -smp 4 -cpu host -vga virtio -display sdl,gl=on
```

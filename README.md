## [How to install KVM on Linux](https://sysguides.com/install-kvm-on-linux)
---
## [How to install a Windows 11 Virtual Machine on KVM](https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm)
---
## [single gpu passthrough github guide](https://github.com/QaidVoid/Complete-Single-GPU-Passthrough)
---
## enabling UEFI support for BIOS

https://github.com/tianocore/tianocore.github.io/wiki/OVMF

more information:

https://wiki.archlinux.org/title/PCI_passthrough_via_OVMF

aur package

https://archlinux.org/packages/extra/any/edk2-ovmf/

---
## How to extend/increase a Windows partition

1. Shutdown the VM

        virsh shutdown hostname

2. Increase the qcow2 image

Find the qcow2 file of the VM and take a backup (just in case).

    cp hostname.qcow2 hostname.qcow2.backup
    qemu-img resize hostname.qcow2 +100GB
    
3. Start the VM

        virsh start hostname

4. Extend the partition in Window

Windows has a really good partition management utility built into it. Search for `disk management`

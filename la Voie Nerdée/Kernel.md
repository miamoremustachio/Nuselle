The core part of an operating system which acts as a bridge between the software and the hardware of a computer

# *Kernel architectures*

## Ⓜ️ Monolithic
- All OS services run in kernel space
- Examples: Unix, Linux, FreeBSD etc.

## 🫆 Microkernel
- Most services run in user space
- Examples: QNX, Minix, Mach

## ☯️ Hybrid kernel
- mixes monolithic + microkernel; some services in kernel for speed, others isolated for safety
- Examples: Windows NT family (Windows 2000, XP, Vista, 7, 8, 10 etc.), macOS, Haiku OS

# 🐧 Linux kernel

The original ("vanilla") Linux kernel is distributed via [kernel.org](https://www.kernel.org/)
To provide software communication with the kernel, Linux use [[POSIX]] standard
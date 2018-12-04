## Real mode
all x86 cpu's start in this mode.

doesn't support paging, uses actual physical addresses

## BIOS
responsible for init the hardware and providing services for the kernel

## Bootloader
responsible for booting
512 bytes located at 0x0000:0x7c00 (0st segment at 0x7c00).
respoonsible for picking the hard drive and partition to boot from.

## Kernel
main part of the operating system.

### Plan
1. write a MBR that copies kernel from HDD to RAM using int 0x13
2. Load into the kernel and pring Hello World using int 0x10

### Process
BIOS -loads-> MBR -loads-> Kernel



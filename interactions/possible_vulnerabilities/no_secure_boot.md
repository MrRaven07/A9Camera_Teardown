# Lack of Cryptographic Secure Boot

As said in [initial_connect.md](../uart2_connect/initial_connect.md), the command `go os_addr(0x10000)` indicated that the bootloader is executing a dumb jump. 

If one extracts the firmware, modifies the RT-Thread OS and flashes it back, the bootloader will directly boot into it.


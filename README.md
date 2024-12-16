# Toolchain RISC-V used

1. git clone
The archive was split into 12 files with `split -b 100M corev-openhw-gcc-ubuntu2004-20211104.tar.gz "corev-openhw-gcc-ubuntu2004-20211104.tar.gz.part"`
2. First combines the 12 files: `cat corev-openhw-gcc-ubuntu2004-20211104.tar.gz.parta* >corev-openhw-gcc-ubuntu2004-20211104.tar.gz`
2. Extract archive `corev-openhw-gcc-ubuntu2004-20211104.tar.gz`
3. It's recommended to move the toolchain at `/opt/corev`, otherwise you should :
    - adapt RISCV in makefile of `execution-integrity-down-to-control-signals` at line `RISCV := /opt/corev`. 
    - adapt step 3 of `linear_code_extraction` README.
4. Toolchain binaries are available at  `/opt/corev/bin/riscv32-corev-elf-gcc`

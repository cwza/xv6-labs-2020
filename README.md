# xv6-labs-2020 Environment Setup
* Course: https://pdos.csail.mit.edu/6.828/2020/

## Clone This Repository
* `git clone <this repository> ~/xv6-labs-2020`

## Install Dependencies
* Use Ubuntu 20.04
``` sh
sudo apt install git build-essential gdb-multiarch qemu-system-misc gcc-riscv64-linux-gnu binutils-riscv64-linux-gnu
sudo apt remove qemu-system-misc
sudo apt install qemu-system-misc=1:4.2-3ubuntu6
sudo apt install python-is-python3
```

## Run xv6
``` sh
make qemu
ls
# use Ctrl-a x to quit qemu
```

## Setup GDB
* Create a terminal and run `make qemu-gdb` or `make CPUS=1 qemu-gdb` to run on single thread mode
* Create another terminal and run `gdb-multiarch`
    + use `file user/_ls` to load module
    + use `b <funcName>` to add break point
    + use `c` to continue

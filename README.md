
# SENG 21213 – Operating Systems Assignment

## project structure

seng21213-os/
│
├── boot/
│   └── boot.asm
│
├── kernel/
│   ├── kernel.c
│   ├── shell.c
│   └── string.c
│
├── drivers/
│   ├── vga/
│   │   └── vga.c
│   └── keyboard/
│       └── keyboard.c
│
├── include/
│   ├── kernel.h
│   ├── vga.h
│   ├── keyboard.h
│   ├── io.h
│   ├── shell.h
│   └── string.h
│
├── Makefile
├── linker.ld
├── README.md
└── .gitignore

---

## Student

Name: Pasindu Chinthaka
Course: SENG 21213 – Operating Systems
University: University of Kelaniya
Repository: Private GitHub Repository

---

## Project Overview

This repository contains my implementation of the Operating Systems assignment for SENG 21213.

The project follows the official SENG 21213 Student Guide and progressively develops a small x86-based operating system from a bootable Stage 0 kernel to a basic file system.

The operating system is implemented using:

* C99
* NASM x86 Assembly
* Make
* QEMU
* GDB

---

## OS Development Stages

Stage 0 - 🔄 In Progress
Boot, VGA & Shell
`v0.1-stage0`

Stage 1 - ⏳ Pending
Process Table & Round-Robin Scheduler
`v0.2-stage1`

Stage 2 - ⏳ Pending
Threads, Mutex & Semaphore
`v0.3-stage2`

Stage 3 - ⏳ Pending
Physical Memory Manager
`v0.4-stage3`

Stage 4 - ⏳ Pending
RAM Disk File System
`v0.5-stage4`

---

## Stage 0 – Boot, VGA & Shell

Stage 0 provides the basic operating system environment.

Implemented components include:

* 512-byte x86 MBR bootloader
* Protected mode transition
* GDT setup
* VGA text-mode driver
* PS/2 keyboard driver
* Interactive kernel shell
* Basic shell commands

### Stage 0 Commands

help
clear
echo
version
colour
halt


---

## Stage 1 – Process Table & Scheduler

Planned components:

* Process Control Block (PCB)
* Process creation
* 4 KB process stacks
* i8253 PIT timer
* IRQ0 timer interrupt
* Context switching
* Round-Robin scheduler
* `ps` command
* `kill` command

Release:

v0.2-stage1

---

## Stage 2 – Threads, Mutex & Semaphore

Planned components:

* Kernel threads
* Thread creation
* Mutex
* Counting semaphore
* Race-condition demonstration
* Producer-consumer problem
* Synchronization

Release:

v0.3-stage2

---

## Stage 3 – Physical Memory Manager

Planned components:

* BIOS E820 memory map
* Physical memory bitmap
* 4 KB page-frame management
* Frame allocation
* Frame deallocation
* Memory information command

Release:

v0.4-stage3

---

## Stage 4 – RAM Disk File System

Planned components:

* 1 MB RAM disk
* Superblock
* Block bitmap
* Inode bitmap
* Inodes
* Flat directory
* File creation
* File reading
* File writing
* File deletion

Shell commands:

ls
touch
cat
write
rm

Release:

v0.5-stage4


---

## Build and Run

Build the operating system:

```bash
make
```

Run in QEMU:

```bash
make run
```

Clean build files:

```bash
make clean
```

Debug using QEMU and GDB:

```bash
make debug
```

In another terminal:

```bash
make gdb
```

---

## Development Environment

The project is developed and tested using:

* Ubuntu / WSL2
* GCC
* NASM
* GNU Make
* QEMU
* GDB
* Git
* GitHub

---

## Repository Rules

Binary build artifacts are not committed to the repository.

The following are ignored:

build/
seng21213.img
*.o
*.bin
*.elf

Only source code, build configuration and documentation required by the assignment are committed.

---

## References

* SENG 21213 Student Guide
* Course lecture materials
* OSDev Wiki
* NASM documentation
* Intel Software Developer Manuals
* Computer Organization and Architecture – William Stallings

---

## Releases

The project will contain five GitHub releases corresponding to the five development stages:

v0.1-stage0
v0.2-stage1
v0.3-stage2
v0.4-stage3
v0.5-stage4

Each release will contain the completed functionality for its corresponding stage.

# Computer System Fundamentals & Internals

Concise, human-friendly notes covering core computer systems topics: hardware, firmware & boot, operating systems, process internals & scheduling, memory management, and device drivers. These notes are organized as short chapter-style Markdown files to help learners and practitioners quickly find and review key concepts.

---

## Repository short description

Computer System Fundamentals and Internals- concise study notes on how computers boot, how operating systems work, and how processes, memory, and devices are managed.

## What’s in this repo

This folder contains a small, curated set of markdown notes designed to teach (or quickly remind) core concepts in computer systems. Files:

- `00.cs-fundamentals.md` — Fundamentals: CPU, memory, storage, buses, and I/O devices. A hardware + software overview and memory/storage hierarchy.
- `01.firmware-and-boot-process.md` — Firmware, POST, bootloaders (GRUB), kernel loading, init/systemd, and the full boot flow from power on to user space.
- `02.the-os.md` — Operating system concepts: kernel vs user space, system calls, process management, memory and file system responsibilities, and device management basics.
- `03.process-internals-and-scheduling.md` — Process lifecycle, creation (fork/exec), context switching, scheduling algorithms, and zombies/orphans.
- `04.memory-management-internals.md` — Virtual memory, paging, page tables, swap, fragmentation, thrashing, and how the OS maps virtual → physical memory.
- `05.device-management-and-drivers.md` — Device drivers, `/dev`, kernel modules, `dmesg`, `udev`, and common device management flows (e.g., plugging a USB drive).

## Who this is for

- Students new to computer systems who want a compact but practical overview.
- Developers who need a quick refresher on OS internals or boot process details.
- Instructors assembling a lightweight course or study guide.

## Suggested study flow

1. Start with [00.cs-fundamentals.md](00.cs-fundamentals.md) — hardware and high-level system context.
2. Read [01.firmware-and-boot-process.md](01.firmware-and-boot-process.md) — firmware, POST and bootloader flow.
3. Read [02.the-os.md](02.the-os.md) — core OS responsibilities and interfaces.
4. Dive into [03.process-internals-and-scheduling.md](03.process-internals-and-scheduling.md) and [04.memory-management-internals.md](04.memory-management-internals.md) — process behavior and memory internals.
5. Finish with [05.device-management-and-drivers.md](05.device-management-and-drivers.md) — device drivers and device management flows.

## How to use these notes

- Open the files in any Markdown viewer or editor (VSCode, Obsidian, or your browser).
- For hands-on learning, on a Linux machine try simple commands mentioned in the notes (`dmesg`, `lsmod`, `lspci`, `free -h`, `pstree`, `swapon` etc.) to connect theory with practice.

## Example quick commands (use in a terminal)

- View boot messages: `dmesg | less`
- List kernel modules: `lsmod`
- Inspect memory: `free -h` or `cat /proc/meminfo`
- Inspect processes: `pstree -p` or `ps aux --sort=-%cpu | head`

## Contributing

- Small improvements (typo fixes, small clarifications) are welcome — open a PR with changes to the relevant `.md` file.
- For larger structural changes or new chapters, open an issue to discuss scope and organization first.

---

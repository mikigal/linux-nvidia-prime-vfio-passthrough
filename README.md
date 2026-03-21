# Linux NVIDIA PRIME Offloading + GPU Passthrough

A comprehensive guide to setting up NVIDIA PRIME offloading alongside GPU passthrough (VFIO, without rebooting) and Looking Glass on Linux systems.

## Setup Assumptions
- By default, the system and applications run on the AMD dGPU or an integrated GPU to ensure maximum compatibility and stability
- The user can run any application on the NVIDIA GPU using PRIME offloading without reconnecting monitors
- It is possible to run a Windows virtual machine with NVIDIA GPU PCIe passthrough without requiring a system reboot
- VM display is handled via Looking Glass with clipboard, high refresh rate, and HDR support
- Minimal performance cost and latency - in testing, I achieved only around 5% lower GPU and CPU performance in the VM compared to bare-metal Windows, and the latency is imperceptible. PRIME offloading does not affect performance at all

## How?
Check [**wiki**](https://github.com/mikigal/linux-nvidia-prime-vfio-passthrough/wiki) for the full guide

## Why?
Windows sucks, and rebooting every time you want to run a game sucks even more.  
Proton is good, but not for all games (mainly DirectX 12), so I want to get as much performance as possible.

## Authors
- [Mikołaj Gałązka](https://github.com/mikigal) - research, testing, scripts, documentation
- [Adam Grzegorzewski](https://github.com/SocketByte) - research, testing, documentation improvements, dvmm tool

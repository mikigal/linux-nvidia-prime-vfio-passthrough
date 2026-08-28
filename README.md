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

## Presentation
https://www.youtube.com/watch?v=KDzlMwB48c4

## Why?
Windows **sucks**, but you know what sucks even more? Dual boot.

Proton has gotten *REALLY* impressive, but there are unfortunately many games (mostly DX12 games on NVIDIA) that run far worse or don't support modern features like DLSS, frame generation or RT/PT on Linux. And what about apps? Photoshop, many CADs or professional applications outright don't support Linux. 

Having an easy to use VM with full performance is really useful, especially considering with this setup you don't have to sacrifice your host performance as well.

## Authors
- [Mikołaj Gałązka](https://github.com/mikigal) - research, testing, scripts, guide
- [Adam Grzegorzewski](https://github.com/SocketByte) - research, testing, guide improvements, dvmm tool

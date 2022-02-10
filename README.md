# WireGuard and Weston's VNC/RDP on TorizonCore
Brief overview regarding how to use VNC with WireGuard on TorizonCore

## Table of Contents
1. [Specs](#specs)
2. [Recommended readings](#readings)
3. [General overview of WireGuard](#overview)
4. [Running WireGuard on Linux ](#wireguard_linux)
    1.  Configuration of the server
    2.  Configuration of the client
    3.  Server-client Connection
5. Running WireGuard on TorizonCore
6. VNC/RDP on TorizonCore
7. Known issues


## Specs
- SoM
  - Colibri iMX8QXP 2GB WB IT V1.0D
- Carrier Board
  - Aster V1.1B
- PC
```
██████████████████  ████████   andre@andre-vostro5490
██████████████████  ████████   ----------------------
██████████████████  ████████   OS: Manjaro Linux x86_64
██████████████████  ████████   Host: Vostro 5490
████████            ████████   Kernel: 5.15.12-1-MANJARO
████████  ████████  ████████   Uptime: 17 mins
████████  ████████  ████████   Packages: 1217 (pacman)
████████  ████████  ████████   Shell: bash 5.1.12
████████  ████████  ████████   Resolution: 1920x1080, 2560x1080
████████  ████████  ████████   DE: Plasma 5.23.4
████████  ████████  ████████   WM: KWin
████████  ████████  ████████   Theme: Breath Light [Plasma], Breeze [GTK2/3]
████████  ████████  ████████   Icons: breeze [Plasma], breeze [GTK2/3]
████████  ████████  ████████   Terminal: konsole
                               CPU: Intel i7-10510U (8) @ 4.900GHz
                               GPU: NVIDIA GeForce MX230
                               GPU: Intel CometLake-U GT2 [UHD Graphics]
                               Memory: 1429MiB / 15787MiB
```
OpenVPN version:  
https://developer.toradex.com/knowledge-base/openvpn-westons-vncrdp-on-torizoncore

WireGuard on TorizonCore:  
https://developer.toradex.com/knowledge-base/how-to-use-vpn-on-torizoncore

## Recommended readings <a name="readings" />
- Basics of VPN concepts  (See Computer Networking: Top-Down Approach, 7th Ed, Kurose, Ross, p. 665)
- Basics of WireGuard
  - [WireGuard: fast, modern, secure VPN tunnel](https://www.wireguard.com/#conceptual-overview)
  - [Routing & Network Namespace - WireGuard](https://www.wireguard.com/netns/)
    - Requires basic knowledge of Linux Namespaces (See Linux Bible, 10th Ed, Negus, p. 695)
  - [Quick Start - WireGuard](https://www.wireguard.com/quickstart/)
- Basics of Docker containers (See Linux Bible, 10th Ed, Negus, p. 693, Ch. 26)
  - [Free Docker Tutorial - Docker Essentials](https://www.udemy.com/course/docker-essentials/)
- Basics of VNC/RDP
  - [Remote Access the TorizonCore GUI Using VNP or RDP](https://developer.toradex.com/knowledge-base/remote-access-to-torizoncore-ui)


## General overview of WireGuard <a name="overview" />


## Running WireGuard on Linux <a name="wireguard_linux" />

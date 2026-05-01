# Eaglercraft (Tuff Client) 1.20.4 Modded Server

A hybrid Minecraft server setup that bridges a **Fabric 1.20.4 modded server** with **Eaglercraft/Tuff Client browser access** through a multi-layer proxy and translation stack.

This project enables modern Minecraft gameplay to be accessed directly from a browser-based client using compatibility layers and protocol translation.

---

## Overview

This server architecture combines multiple systems to achieve cross-version and cross-platform compatibility:

- Modern **Fabric 1.20.4** Minecraft server backend
- Proxy-based connection handling via Velocity
- Protocol translation for version compatibility
- Content mapping for items, blocks, and registries
- Browser-based client support via WebSocket (wss)

---

## Features

- **1.20.4 Minecraft server experience**
- Browser-compatible multiplayer via Tuff/Eagler clients
- Cross-version support using translation layers
- Mod support via PolyMc (limited compatibility)
- Optimized server performance using Lithium
- Proxy-based architecture for scalability
- Supports modern gameplay mechanics (including post-1.13 movement such as swimming), with behavior translation handled by TuffX+ for compatibility with Eagler/Tuff clients.

---

## Compatibility Notes

- Designed for **Tuff Client (Eaglercraft-based 1.12.2 client environment)**
- Not all Fabric mods are compatible due to client-side limitations
- Some modern Minecraft features may be visually or functionally simplified
- Client-side rendering and networking behavior may differ from Java Edition

---

## Architecture

This project uses a multi-layer system:

- **Fabric Server** → Game logic and world simulation  
- **Velocity Proxy** → Network routing and client bridging  
- **ViaVersion / ViaBackwards** → Protocol translation between versions  
- **PolyMc** → Item/block/registry mapping for cross-version support  
- **TuffX+** → Eagler/Tuff-specific compatibility enhancements  
- **Tuff Client** → Browser-based Minecraft client interface  

---

## Setup Instructions (Codespaces)

1. Create a GitHub Codespace from this repository  
2. Open a new terminal  
3. Start the Fabric server:
   `cd server && java -jar server.jar`
4. Wait until the server fully initializes  
5. Open a second terminal  
6. Start the Velocity proxy:
   `cd velocity && java -jar velocity.jar`
7. Wait until the proxy fully initializes  
8. Set port **8081** to Public visibility in Codespaces  
9. Copy the generated `wss://` WebSocket URL from the site on port 8081  
10. Connect using **Tuff Client**

---

## Client Access

Play Tuff Client here:  
https://test.tuffis.online

---

## Performance & Stability

- Performance depends on proxy load and translation overhead
- Large player counts may increase desync risk
- Some modded content may require manual mapping adjustments
- Best experience achieved with lightweight Fabric mod configurations

---

## Credits

- Fabric — Fabric server and modding platform  
- Velocity — Proxy and routing layer  
- ViaVersion / ViaBackwards — Protocol translation system  
- PolyMc — Cross-version content mapping  
- Lithium — Server performance optimization  
- EaglerXVelocity — Browser client integration layer 

---

## License / Usage

This project is intended for educational and experimental use involving cross-version Minecraft networking and browser-based client integration.

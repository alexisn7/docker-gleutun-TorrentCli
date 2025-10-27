# 🧱 Docker Gluetun + qBittorrent

This project provides a ready-to-use **Docker Compose stack** for running **qBittorrent** (BitTorrent client) securely through a **VPN tunnel managed by Gluetun**.  
It supports **ProtonVPN** and other VPN providers using **WireGuard** or **OpenVPN**.

---

## 🚀 Features

- ✅ qBittorrent BitTorrent client  
- 🛡️ Gluetun VPN container (ProtonVPN, Mullvad, Private Internet Access, etc.)  
- 🔒 All traffic routed through a secure VPN tunnel  
- 🔁 Port forwarding support  
- ⚙️ Easy configuration via `.env` file  

---

## 🧩 Clone the Repository

If this repository includes submodules (e.g., for `qbittorrent-port-forward-gluetun-server`), make sure to clone it **recursively**:

```bash
git clone --branch qbittorrent --recurse-submodules https://github.com/docker-gleutun-TorrentCli.git
cd docker-gleutun-TorrentCli
```

If you already cloned it without submodules, initialize them manually:

```bash
git --branch qbittorrent submodule update --init --recursive
```

---

## ⚙️ Quick Start

1. Copy the example environment file:

   ```bash
   cp .env.example .env
   ```

2. Edit `.env` and set your VPN credentials and preferences.

3. Start the stack:

   ```bash
   docker-compose up -d
   ```

4. Access the **qBittorrent Web UI** at:  
   👉 [http://localhost:65534](http://localhost:65534)

---

## 📁 Project Structure

| File | Description |
|------|--------------|
| `docker-compose.yml` | Main Docker Compose configuration |
| `.env.example` | Example environment variables template |
| `.env` | Your environment configuration file |
| `qbittorrent-port-forward-gluetun-server/` | Port forwarding helper submodule |

---

## 📚 References

- [🔗 Gluetun Wiki](https://github.com/qdm12/gluetun-wiki)
- [🐧 LinuxServer qBittorrent](https://github.com/linuxserver/docker-qbittorrent)
- [🌀 Port Forward Helper (by mjmeli)](https://github.com/mjmeli/qbittorrent-port-forward-gluetun-server)

---

## 🧾 License

**MIT License**

```
MIT License  
Copyright (c) 2025  

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE  
SOFTWARE.
```


# Docker Gleutun Transmission

This project provides a ready-to-use Docker Compose stack for running qbittorrent (BitTorrent client) securely through a VPN using Gluetun. It supports ProtonVPN and other providers, with WireGuard or OpenVPN.

## Features

- Qbittorrent BitTorrent client
- Gluetun VPN container (ProtonVPN, WireGuard, OpenVPN, etc.)
- All traffic routed through VPN
- Port forwarding support
- Easy configuration via `.env` file

## Quick Start

1. Copy the example environment file:

 ```sh
 cp .env.example .env
 ```

2. Edit `.env` with your VPN credentials and preferences.
3. Start the stack:

 ```sh
 docker-compose up -d
 ```

4. Access Transmission Web UI at [http://localhost:65534](http://localhost:65534)

## Files

- `docker-compose.yml`: Main compose file
- `.env.example`: Example environment variables template
- `.env`: Your environment variables for configuration

## References

- [Gluetun Wiki](https://github.com/qdm12/gluetun-wiki)
- [LinuxServer Qbittorrent](https://github.com/linuxserver/docker-qbittorrent)

---
MIT License

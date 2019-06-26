# Project V

Project V is a set of tools to help you build your own privacy network over internet. The core of Project V, named V2Ray, is responsible for network protocols and communications. It can work alone, as well as combine with other tools.

## Features

- Multiple inbound/outbound proxies: one V2Ray instance supports in parallel multiple inbound and outbound protocols. Each protocol works independently.
- Customizable routing: incoming traffic can be sent to different outbounds based on routing configuration. It is easy to route traffic by target region or domain.
- Multiple protocols: V2Ray supports multiple protocols, including Socks, HTTP, Shadowsocks, VMess etc. Each protocol may have its own transport, such as TCP, mKCP, WebSocket etc.
- Obfuscation: V2Ray has built in obfuscation to hide traffic in TLS, and can run in parallel with web servers.
- Reverse proxy: General support of reverse proxy. Can be used to build tunnels to localhost.
- Multiple platforms: V2Ray runs natively on Windows, Mac OS, Linux, etc. There is also third party support on mobile.

## Links

[Homepage](https://www.v2ray.com/en/)
[Github Repository](https://github.com/v2ray/v2ray-core)
[Unofficial Chinese manual](https://toutyrater.github.io/)

## Installation

### Linux

```sh
bash <(curl -L -s https://install.direct/go.sh)
```

The script installs the following files.

- `/usr/bin/v2ray/v2ray`: V2Ray executable
- `/usr/bin/v2ray/v2ctl`: Utility
- `/etc/v2ray/config.json`: Config file
- `/usr/bin/v2ray/geoip.dat`: IP data file
- `/usr/bin/v2ray/geosite.dat`: domain data file

This script also configures V2Ray to run as service, if systemd is available.

Configurations are at the following places.

- `/etc/systemd/system/v2ray.service`: Systemd
- `/etc/init.d/v2ray`: SysV

After installation, we will need to:

1. Update `/etc/v2ray/config.json` file for your own scenario.
2. Run `service v2ray start` command to start V2Ray.
3. Optionally `run service v2ray start|stop|status|reload|restart|force-reload` to control V2Ray service.

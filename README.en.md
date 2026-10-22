<div align="center">

# EasyGRC

**A governance, risk and compliance platform.**

[![Latest version](https://img.shields.io/github/v/release/whoami-ru/EasyGRC-Free-Releases?label=version&color=2ea043)](https://github.com/whoami-ru/EasyGRC-Free-Releases/releases/latest)
[![Licence](https://img.shields.io/badge/licence-PolyForm%20Strict%201.0.0-blue)](#licence)
[![Linux x86_64](https://img.shields.io/badge/Linux-x86__64-lightgrey)](#requirements)

[**Download the latest version**](https://github.com/whoami-ru/EasyGRC-Free-Releases/releases/latest) · [Русский](README.md) · [Suggest an improvement](https://github.com/whoami-ru/EasyGRC-Free-Releases/issues/new/choose)

[**Official Websites**](https://easygrc.kz)

</div>

---

## Install in 3 steps

**1. Download** `easygrc-<version>-free.tar.gz` and its `.sha256` file from the [Releases](https://github.com/whoami-ru/EasyGRC-Free-Releases/releases/latest) page.

**2. Check the download** (on the server, both files in the same folder):

```bash
sha256sum -c easygrc-<version>-free.tar.gz.sha256
```

It must print `OK`. If it does not, download the file again.

**3. Install:**

```bash
sudo mkdir -p /opt/easygrc
sudo tar -xzf easygrc-<version>-free.tar.gz -C /opt/easygrc --strip-components=1
cd /opt/easygrc
sudo ./install.sh
```

The script checks the server, installs Docker if needed, loads the images, asks for the language and a domain name, creates the settings and a certificate, starts the system and offers to create the first administrator. Then open `https://<server address>/`.

The full guide (domain and certificate, backups, troubleshooting) is in the archive as `INSTALL.en.md`.

## Requirements

- Linux x86_64: Ubuntu 22.04+, Debian 12+, AlmaLinux/Rocky/RHEL 9+ or similar. Windows and macOS are not supported.
- 2 vCPU, 4 GB of memory, 20 GB of disk. A trial run is fine with 1 GB of memory and 2 GB of swap.
- Ports 80 and 443. A domain name is optional: without one the system opens by IP address.
- Not sure the server will do? Run `sudo ./install.sh --check`. It changes nothing and shows what is missing.


## Suggestions and questions

Found a bug, missing a feature, or something in the installation is unclear? [Open an issue](https://github.com/whoami-ru/EasyGRC-Free-Releases/issues/new/choose), there are templates. Attach the version from the `VERSION` file and never post `.env`, passwords or keys.

Report vulnerabilities privately, not in an issue: [SECURITY.md](SECURITY.md).

## Licence

The software is provided under [PolyForm Strict 1.0.0](https://polyformproject.org/licenses/strict/1.0.0): you may use it for noncommercial purposes, but not distribute or modify it. The full text is in the `LICENSE` file inside the archive. This repository holds only the description and the releases, there is no source code here.

Want to hear about new versions? Click **Watch → Custom → Releases** at the top of the page.

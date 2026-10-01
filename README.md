# Brazy-Tool
A tool that scans ip with a lot info
# Brazy

**Lab Recon Console** — a lightweight desktop tool for TCP connect sweeps and banner grabbing against lab and CTF targets you're authorized to test.

---

## What it does

Brazy combines two common first steps of network reconnaissance in one simple graphical app:

- **TCP connect sweep:** checks which TCP ports on a target are open by completing a normal TCP handshake (a "connect" scan). It needs no root privileges or raw sockets, so it runs as a regular user.
- **Banner grabbing:** connects to open ports and reads the greeting or banner a service sends back (e.g. SSH, FTP, SMTP, HTTP server headers). This helps you identify what software, and often which version, is running.

## What it's useful for

- **CTFs and practice labs:** quickly map a box on HackTheBox, TryHackMe, VulnHub, or your own VMs before digging deeper.
- **Home labs:** verify which services your machines actually expose.
- **Learning:** see how TCP connect scanning and service identification work without memorizing command-line flags.
- **Quick checks:** a fast, GUI-first alternative when you don't need a full-featured scanner.

## Installation

> Brazy targets Linux desktops that follow the freedesktop.org standards (GNOME, KDE, XFCE, etc.).

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/brazy-tool.git
   cd brazy-tool
   ```

2. Install the executable to your local bin directory:
   ```bash
   mkdir -p ~/.local/bin
   cp brazy ~/.local/bin/brazy
   chmod +x ~/.local/bin/brazy
   ```
   Make sure `~/.local/bin` is on your `PATH`.

3. Install the desktop entry and icon so Brazy shows up in your app launcher:
   ```bash
   mkdir -p ~/.local/share/applications ~/.local/share/icons/hicolor/256x256/apps
   cp brazy.desktop ~/.local/share/applications/
   cp brazy.png ~/.local/share/icons/hicolor/256x256/apps/brazy.png
   update-desktop-database ~/.local/share/applications 2>/dev/null || true
   ```

Brazy will now appear under **Network** / **Security** in your application menu. You can also find it by searching for terms like *recon*, *scan*, *ports* or *banner*.

## Usage

Launch **Brazy** from your application menu, or run:

```bash
brazy
```

Then:

1. Enter a target host or IP address.
2. Choose the ports or port range to sweep.
3. Start the scan. Open ports are listed along with any banners the services return.

<!-- TODO: add screenshots and describe any options (timeouts, threads, export, etc.) -->

## Requirements

<!-- TODO: fill in the language/runtime and dependencies, e.g. Python 3.x + GTK/Qt -->
- Linux with a freedesktop-compatible desktop environment
- _Runtime and dependencies: TBD_

## ⚠️ Legal and ethical use

Brazy is intended **only** for systems you own or have explicit, written permission to test, such as your own lab machines, CTF targets and authorized engagements.

Scanning networks or hosts without authorization may be illegal in your jurisdiction and may violate the terms of service of your ISP or hosting provider. You are solely responsible for how you use this tool. The authors accept no liability for misuse.

## Contributing

Issues and pull requests are welcome. If you find a bug or have a feature idea, please open an issue.

## License

<!-- TODO: choose a license, e.g. MIT -->
_TBD_

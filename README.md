# ansible-cursor

An Ansible playbook for installing and updating the Cursor editor on Linux systems.

## Description

This repository contains an Ansible playbook that automates the installation and updating of the Cursor editor on Linux systems. The playbook handles:
- Downloading the latest stable version of Cursor
- Installing it as an AppImage
- Setting up desktop integration
- Supporting both x86_64 and ARM64 architectures

## Requirements

- Ansible 2.9 or higher
- Linux operating system
- Internet connection for downloading Cursor

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/jefferyb/ansible-cursor.git
   cd ansible-cursor
   ```

2. Run the playbook:
   ```bash
   ansible-playbook install-cursor.yaml
   ```

## Usage

### Local Installation
To install or update Cursor on your local machine:
```bash
ansible-playbook install-cursor.yaml
```

### Remote Installation
To install Cursor on a remote machine:
```bash
ansible-playbook install-cursor.yaml -e host=your-remote-machine
```

## What the Playbook Does

1. Creates necessary directories in `~/.local/opt/cursor`
2. Fetches the latest Cursor download URL from the official API
3. Downloads the appropriate AppImage for your architecture
4. Sets up the desktop integration with icon and menu entry
5. Makes the AppImage executable

## Architecture Support

The playbook supports the following architectures:
- x86_64 (amd64)
- aarch64/arm64

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

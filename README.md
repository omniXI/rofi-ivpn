# IVPN Rofi Menu

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Shell: Bash](https://img.shields.io/badge/Shell-Bash-blue.svg)](https://www.gnu.org/software/bash/)
[![Dependencies: IVPN CLI](https://img.shields.io/badge/Dependencies-IVPN%20CLI-green.svg)](https://www.ivpn.net/apps-linux/)

A simple and efficient way to manage your IVPN connection using Rofi. This script provides a user-friendly interface to control your IVPN VPN connection through a Rofi menu.

## Features

- Quick connect to fastest server
- Server selection with search functionality
- Firewall management
- Connection status display
- Disconnect option

## Installation

1. Clone the repository:
```bash
git clone https://github.com/omniXI/rofi-ivpn.git
cd ivpn-rofi
```

2. Make the script executable:
```bash
chmod +x rofi-ivpn.sh
```

3. Run the script:
```bash
./rofi-ivpn.sh
```

## Usage

### Navigation
- Use arrow keys to navigate
- Type to search servers
- Enter to select
- Esc to exit

### Menu Structure

#### Main Menu
```
[Status: CONNECTED Singapore]
Quick Connect
Servers
Firewall
Disconnect
```

#### Server Selection
```
[Search/Filter: ]
WireGuard | Singapore (SG)
WireGuard | Tokyo (JP)
OpenVPN | London (UK)
...
```
- Type to filter by country/location
- Shows protocol, location, and country
- Select to connect to specific server

#### Firewall Menu
```
[Firewall Status: Enabled]
Enable Firewall
Disable Firewall
Allow LAN
Block LAN
Allow IVPN Servers
Block IVPN Servers
```

## Menu Options

### Quick Connect
- Connects to the fastest available server
- Uses `ivpn connect -f`

### Servers
- Shows list of all available servers
- Displays protocol, location, and country
- Search functionality to filter servers
- Select to connect to specific server

### Firewall
- Enable/Disable IVPN firewall
- Control LAN access
- Manage IVPN server access
- All changes take effect immediately

### Disconnect
- Disconnects from current VPN server
- Uses `ivpn disconnect`

## Requirements

- [IVPN CLI](https://www.ivpn.net/apps-linux/) - IVPN's command-line interface
- [Rofi](https://github.com/davatorium/rofi) - A window switcher, application launcher and dmenu replacement
- Bash - The GNU Bourne Again Shell

## Notes

- The script uses the IVPN CLI command `ivpn`
- Server list updates automatically
- Status shows current connection state and country
- All commands are executed through the IVPN CLI

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# Networkmanager-dmenu

Manage NetworkManager connections with dmenu, [Rofi][1] instead of nm-applet

## Features

- Doesn't require a config, sensible defaults
- Connect to existing NetworkManager wifi or wired connections
- Connect to new wifi connections. Requests passphrase if required
- Connect to _existing_ VPN, Wireguard, GSM/WWAN and Bluetooth connections
- Enable/Disable wifi, WWAN, bluetooth and networking
- Launch nm-connection-editor GUI
- Support for multiple wifi adapters
- Optional Pinentry support for secure passphrase entry
- Delete existing connections
- Rescan wifi networks
- Uses notify-send for notifications if available

![Screencast](nmdm.gif)

## Installation

- Copy script somewhere into $PATH

## Requirements

1. Python 3.7+
2. NetworkManager
3. Rofi (X or XWayland)
4. Python gobject (PyGObject, python-gobject, etc.)
5. (Debian/Ubuntu based distros) libnm-util-dev and gir1.2-nm-1.0 (you have to
   explicitly install the latter on Debian Sid)
6. (optional) The network-manager-applet package (in order to launch the GUI
   connection editor, if desired. The nm-applet does _not_ need to be started.)
8. (optional) ModemManager for WWAN support.
9. (optional) notify-send for notifications (connected, disconnected, etc.)

## Usage

`networkmanager_dmenu [-h] <menu args>`

- Run script or bind to keystroke combination
- If desired, menu options can be passed on the command line instead of or in
  addition to the config file. These will override options in the config file.

## MIT License

[1]: https://davedavenport.github.io/rofi/ "Rofi"

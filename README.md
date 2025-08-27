# Hostfile
Annoying to add hostfile everytime.
## Usage:

```bash
$ hostfile
Usage:
  hostfile [--linux|--windows] <IP> <DOMAIN> [SHORTNAME]
    Adds or updates an entry in the hosts file.

  hostfile [--linux|--windows] -R <DOMAIN or SHORTNAME>
    Removes any entry containing the specified domain or hostname.

  hostfile --setup
    Installs this script to /usr/bin/hostfile with proper permissions (requires sudo).

  hostfile -h | --help
    Show this help message.

Examples:
  # Add AD box entry on Linux (with shortname):
  ./hostfile --linux 10.10.10.5 dc.htb.local dc

  # Add normal Linux box entry (no shortname):
  ./hostfile --linux 10.10.10.10 hack.htb

  # Add Windows hosts entry (via WSL):
  ./hostfile --windows 10.10.10.10 hack.htb

  # Remove entry by domain or shortname:
  ./hostfile --linux -R hack.htb
  ./hostfile --linux -R dc

  # Setup the script (move to /usr/bin and set permissions):
  sudo chmod +x hostfile
  sudo ./hostfile --setup
```

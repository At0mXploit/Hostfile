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
  ./hostfile.sh --linux 10.10.10.5 dc.htb.local dc

  # Add normal Linux box entry (no shortname):
  ./hostfile.sh --linux 10.10.10.10 hack.htb

  # Add Windows hosts entry (via WSL):
  ./hostfile.sh --windows 10.10.10.10 hack.htb

  # Remove entry by domain or shortname:
  ./hostfile.sh --linux -R hack.htb
  ./hostfile.sh --linux -R dc

  # Setup the script (move to /usr/bin and set permissions):
  sudo ./hostfile.sh --setup
```

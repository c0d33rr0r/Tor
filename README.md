## What is TorGhost ?
TorGhost is an anonymization script. TorGhost redirects all internet traffic through SOCKS5 tor proxy. DNS requests are also redirected via tor, thus preventing DNSLeak. The scripts also disables unsafe packets exiting the system. Some packets like ping request can compromise your identity.

ArchTorGhost is a MOD for arch users n the above!

Must be using BASH | ZSH
## How to install Arch?

`sudo sudo pacman -Sy tor python-stem python-requests python-packaging cython`

`mkdir build`

`cd build`

`py3_version=$(python3 -V | cut -d' ' -f2 | cut -d'.' -f1,2)`

`cython ../archtorghost.py --embed -o archtorghost.c --verbose`

`gcc -Os -I /usr/include/python${py3_version} -o archtorghost archtorghost.c -lpython${py3_version} -lpthread -lm -lutil -ldl`

`sudo cp -r archtorghost /usr/bin/`

## Usage
ArchTorghost v3.0 usage:

`  -s      --start        Start ArchTorghost`

`  -r      --switch       Request new tor exit node`

`  -x      --stop         Stop ArchTorghost`

## How to install Linux?

`sudo sudo apt install tor python-stem python-requests python-packaging cython`

`mkdir build`

`cd build`

`py3_version=$(python3 -V | cut -d' ' -f2 | cut -d'.' -f1,2)`

`cython ../torghost.py --embed -o torghost.c --verbose`

`gcc -Os -I /usr/include/python${py3_version} -o torghost torghost.c -lpython${py3_version} -lpthread -lm -lutil -ldl`

`sudo cp -r torghost /usr/bin/`

## Usage
Torghost v3.0 usage:

`  -s      --start        Start Torghost`

`  -r      --switch       Request new tor exit node`

`  -x      --stop         Stop Torghost`

`  -h      --help         Print this help and exit`

`  -u      --update       Checks for updates`~~

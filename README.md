
# evec: CLI interface for Eve

```
usage: evec [-h] [-p PLATFORM] [-r REPO] [--proxy PROXY] [--no-cookies]
            {configure,builds,status,restart,watch,force} ...

CLI interface for Eve

optional arguments:
  -h, --help            show this help message and exit
  -p PLATFORM, --platform PLATFORM
  -r REPO, --repo REPO
  --proxy PROXY         Direct traffic through a SOCKS of HTTP proxy. Must be
                        in the format socks(4|5)://host:port or
                        http(s)://host:port
  --no-cookies          Disable persistent cookies for this session

subcommands:
  {configure,builds,status,restart,watch,force}
    configure           Bootstrap CLI configuration
    builds              List all running builds and statuses.
    status              Get the status of a Eve build
    restart             Restart an Eve build
    watch               Watch an Eve build, restarting it if it fails.
    force               Force start an Eve build
```

## Installation
Installation is as simple as

```shell
  curl https://raw.githubusercontent.com/tmacro/evec/master/evec > evec
```

Evec is written to require no dependecies except the standard library for most use cases.
Its only optional dependency is [PySocks](https://github.com/Anorov/PySocks) for SOCKS4/5 proxy support. It can be installed from PyPi using

```
pip install pysocks
```

## Configuration
A interactive configuration prompt can be started with `evec configure`. Configuration and persistent cookies are stored in `~/.eve/eve.ini` and `~/.eve/cookies.txt` respectively.

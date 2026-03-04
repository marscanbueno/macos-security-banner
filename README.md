# macOS Security Banner

![Platform](https://img.shields.io/badge/platform-macOS-lightgrey)
![Shell](https://img.shields.io/badge/shell-bash-blue)
![Purpose](https://img.shields.io/badge/purpose-security--banner-orange)

This repository installs a macOS login policy banner along with supporting system files used in a managed environment.

The scripts included here install:

- a login Policy Banner
- a hosts file
- a Message of the Day (motd)

These files are copied into their standard macOS locations and basic system caches are refreshed after installation.

---
## Installation

> Warning:
> 
> If you plan to run the scripts in this repository, make sure you understand the commands being executed.
>   
> Do not blindly run scripts from the internet. Review them first and run them at your own risk.

You can clone the repository anywhere you like.

A common location is:

```
~/.dotfiles
```

To install using the bootstrap script:

```bash
curl -LJO https://raw.githubusercontent.com/marscanbueno/shared/main/.install.sh && source .install.sh
```

*I updated the repo name as well as the README, you will have to modify the codeblock above.*

---

## Files Installed

The scripts install the following files:

```
/Library/Security/PolicyBanner.rtfd
/etc/hosts
/etc/motd
```

After installation the script also:

- flushes the macOS DNS cache
- updates the APFS preboot volume
- removes the temporary staging directory

***
## Notes

Administrative privileges are required because the scripts modify protected system locations.

Always review scripts before running them with sudo.

***
## Thanks to…

* [Mathias Bynens](https://mathiasbynens.be/) and his [dotfiles repository](https://github.com/mathiasbynens/dotfiles/)
* [Kevin Suttle](http://kevinsuttle.com/) and his [dotfiles repository](https://github.com/kevinSuttle/dotfiles) and [macOS-Defaults project](https://github.com/kevinSuttle/macOS-Defaults)
* [Armin Briegel](https://scriptingosx.com/) and his [repositories](https://github.com/scriptingosx?tab=repositories)
* [Stephen Black](https://stevenblack.com) and his [hosts repositories](https://github.com/StevenBlack/hosts)
# Installing Packages

**What's a Package Manager?**

A package manager serves as the onboard tool for accessing online software catalogs and installing, updating and removing packages from your Linux environment.

There's more than one package manager on the market, and their packages aren't easily cross-compatible. Furthermore, not all packages exist in every package manager's catalog.

Common package management systems include:
- dkpg: Used by Debian and Ubuntu, and supported by tools like apt, aptitude, and the Synaptic Package Manager
- Pacman: Used by Arch Linux
- Portage: Used by Gentoo Linux
- Snappy: A relatively new, self-contained package format developed by Ubuntu's parent company
- RPM Package Manager: Developed by Red Hat and supported by tools like YUM and zypper

**Installing via Commandline**
```bash
# update installed packages / online repositories
sudp apt-get upgrade    # upgrade installed packages
sudo apt-get update     # update online repositories

# search new packages
sudo apt-cache search <keyword>       # search keyword
sudo apt-cache search "web browser"   # search "web browser"-packages
sudo apt-cache show <package name>    # show info about a given package
sudo apt-cache show pwgen             # show info about "pwgen"

# install new packages
sudo apt-get install pwgen   # installs "pwgen"-package
which pwgen                  # display path to pwgen
sudo apt-get install pw      # doubletab to see all packages starting with "pw"

# removing packages
sudo apt-get remove <package name>  # removes package
sudo apt-get purge <package name>   # removes package and related files

# reinstall a package (when its somehow broken)
sudo apt-get install <package name> --reinstall

# remove unneeded cache files stored at /var/cache/apt/packages
sudo apt-get clean    

```

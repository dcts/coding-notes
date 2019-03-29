# Installation

- NODEJS: server side programming in javascript!
- NPM: Node Package Manager allows to download and install npm packages
- NVM: Node Version Manager: allows you to have multiple node versions installed and switch between versions

### NODEJS



### NVP



### NVM 

```bash
# installing required packages for nvm as well as nvm itself (node version manager)
sudo apt-get update
sudo apt-get install build-essential checkinstall libssl-dev
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.32.1/install.sh | bash 

# check if nvm is installed
command -v nvm  # should output nvm

# list all versions availible
nvm ls
nvm ls-remote

# change version
nvm install <x.y.z>       # install specified version x.y.z of node or npm
nvm use <x.y.z>           # use version of node in current terminal
nvm alias default <x.y.z> # set default version
```

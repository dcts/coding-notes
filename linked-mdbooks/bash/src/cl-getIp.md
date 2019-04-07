# getIp

```bash
# WHAT IS MY IP? -> doesnt work!
wget http://Www.whatismyip.com -O - -o /dev/null | grep '<TITLE>' | sed -r 's/<TITLE>WhatIsMyIP\.com \- //g' | sed -r 's/<\/TITLE>//g'

# get public ip
alias ippub="curl https://api.ipify.org/ && echo "; # echo to avoid % at end

# get local ip
alias iploc="ifconfig | grep -Eo 'inet (addr:)?([0-9]*\.){3}[0-9]*' | grep -Eo '([0-9]*\.){3}[0-9]*' | grep -v '127.0.0.1'";
```


# getIp

```bash
# WHAT IS MY IP? -> doesnt work!
wget http://Www.whatismyip.com -O - -o /dev/null | grep '<TITLE>' | sed -r 's/<TITLE>WhatIsMyIP\.com \- //g' | sed -r 's/<\/TITLE>//g'
```


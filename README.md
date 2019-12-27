# esp32 react-hello

Example of hosting a react (https://reactjs.org) project on an ESP32

## esp32 configuration as web server

* Async Web Server
```
#include "WiFi.h"
#include "SPIFFS.h"
#include "ESPAsyncWebServer.h"
#include <ESPmDNS.h>
```
Wifi.h 
* Needed to configure the wifi.
  * SSID
  * Password 

SPIFFS.h SPI Flash File System (https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/storage/spiffs.html)
* Total Flash Size is 16mb but Arduino can only acces 4mb (Not confirmed by testing)
* Tutorial: https://techtutorialsx.com/2019/02/23/esp32-arduino-list-all-files-in-the-spiffs-file-system/
* Library: https://github.com/pellepl/spiffs 
* Place to store files being served
* Doesn't support directories but supports naming with slashes.

ESPAsyncWebServer.h Asyn Web Server
* Library: https://github.com/me-no-dev/ESPAsyncWebServer
* 
* TODO: enable ssl


Enable mDNS
* `#include <ESPmDNS.h>`

React Web Files:
* index.html
* app.js


## React Hello world

* Create React App Tutorial: https://github.com/facebook/create-react-app#getting-started
* Minify using `npm run build`
* We'll run this on the esp32 but could be run locally with:
```
 npm install -g serve
 serve -s build
```


## References
* http://www.react.express/

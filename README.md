# resin-electronjs

a boilerplate for developing kiosks, digital signage or other human-machine interaction projects based on [ElectronJS](http://electron.atom.io/) and [resin.io](http://resin.io)

### PRE-REQUISITES
this application is meant to be deployed to [RaspberryPi2](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/) devices via [resin.io](http://resin.io).

At least 128MB of GPU-dedicated RAM is required. You can achieve this following [this instructions](http://docs.resin.io/#/pages/hardware/i2c-and-spi.md#raspberry-pi-camera-module) - only the first parameter `gpu_mem=128` is required

### WHY THIS TEMPLATE

Achieving kinda-smooth desktop application display on a raspberrypi is hard. This project aims to provide a quickstart template - the magic is in the Dockerfile

### URL LAUNCHER config via ENV VARS

* **`URL_LAUNCHER_URL`** *string* - the URL to be loaded. use `file://app/index.hmtl` to load a local electronJS (or any website) app - *defaults to* `http://resin.io`
* **`URL_LAUNCHER_NODE`** *bool* (converted from *string*) - whether or not enable nodejs - *defaults to* `false`
* **`URL_LAUNCHER_KIOSK`** *bool* (converted from *string*) - whether or not enter KIOSK mode - *defaults to* `true`
* **`URL_LAUNCHER_TITLE`** *string* - the title of the window. Seen only with `URL_LAUNCHER_FRAME`=`true` - *defaults to* `RESIN.IO`
* **`URL_LAUNCHER_FRAME`** *bool* (converted from *string*) - set to "true" to display the window frame. Seen only with `URL_LAUNCHER_KIOSK`=`false` - *defaults to*  `false`
* **`URL_LAUNCHER_CONSOLE`** *bool* (converted from *string*) - set to "true" to display the debug console -  *defaults to*  `false`
* **`URL_LAUNCHER_WIDTH`**  *int* (converted from *string*) -  - *defaults to* `1920`
* **`URL_LAUNCHER_HEIGHT`**  *int* (converted from *string*) -  - *defaults to* `1080`
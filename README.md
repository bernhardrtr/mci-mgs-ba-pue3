# mci-mgs-ba-pue3
MCI Course | Hardware-Related Software Development - Programming Exercise 3

## Installation

### VS Code

#### Python

- Download and install the current [Python](https://www.python.org/downloads/) version.

#### Node.JS

- Download and install [Node.JS](https://nodejs.org/en/).
- Configure Node.js native addon build tool. [See](https://github.com/nodejs/node-gyp#on-windows) for additional information.
  - Install Visual C++ Build Environment: [Visual Studio Build Tools](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools) (using "Visual C++ build tools" workload) or [Visual Studio Community](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community) (using the "Desktop development with C++" workload)
  - Launch cmd, `npm config set msvs_version 2017`
  - Set the Python executeable path, `npm config set python /path/to/python.exe`

#### Visual Studio Code

- Download and install [VS Code](https://code.visualstudio.com/download)

##### Extension PyMakr

- Install the extension PyMakr within VS Code.
- Edit the global settings (`STRG`+`SHIFT`+`P` -> `Pymakr > Global settings`). In `pymakr.json` edit the following lines:
  ```
  ...
	"address": "",
	"username": "",
	"password": "",
  ...
	"autoconnect_comport_manufacturers": [
		"Pycom",
		"Pycom Ltd.",
		"FTDI",
		"Microsoft",
		"Microchip Technology, Inc.",
		"1a86",
		"Silicon Labs"
	]
  ...
  ```

#### MicroPython Stubs

- Clone the [micropython-stubs](https://github.com/Josverl/micropython-stubs) repository next to your MicroPython projects.
  `git clone https://github.com/Josverl/micropython-stubs.git`
- Add the file `.vscode/settings.json` to your project. This is an ESP32 specific configuration example:
  ```
  {
    "python.languageServer": "Pylance",
    "python.autoComplete.extraPaths": [
        "../micropython-stubs/stubs/cpython_core-pycopy",
        "../micropython-stubs/stubs/micropython-v1_18-frozen/esp32/GENERIC",
        "../micropython-stubs/stubs/micropython-v1_18-esp32",
    ],
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": true,
    "python.jediEnabled": false,
  }
  ```

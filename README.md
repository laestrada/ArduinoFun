# Arduino Fun
## Setting up Development Environment on MacOS
1. Install the arduino vscode extension `vsciot-vscode.vscode-arduino`
1. Install the arduino-cli using brew:
```
$ brew update
$ brew install arduino-cli
```
1. Enter in the following commands after plugging in your arduino:
```
$ arduino-cli config init (this step may not be necessary)
$ arduino-cli board list (to get the core version)
$ arduino-cli core install <insert-core-version-here>
```
1. Add the following settings to .vscode/settings.json:
```
}
    "arduino.path": "/opt/homebrew/bin/",
    "arduino.commandPath": "arduino-cli",
    "arduino.useArduinoCli": true
}
```
1. Restart vscode
1. Run Arduino: Initialize from the command pallet
1. Select your board, programmer, and serial output if different from .vscode/arduino.json

Note: attempted to create a devcontainer, but currently the --device keyword for docker run is not supported on MacOS, see this [issue](https://github.com/docker/for-mac/issues/900)

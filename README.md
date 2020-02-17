# Yet Another Firmware Selector

A simple OpenWrt firmware selector using autocompletion. Uses plain HTML/JavaScript.

![image](misc/screenshot.png)

Checkout the [Demo](https://mwarning.github.io/yet_another_firmware_selector/)!

Run:

* Download repository and change directory to it
* Start webserver (e.g. `python3 -m http.server`)
* Go to `http://localhost:8000`

Configure with [config.js](config.js).

## Update Database

The `names-<version>.json` files are based on JSON files created by OpenWrt (master): `Global build settings  ---> [*] Create JSON info files per build image`.

A [Python script](misc/collect.py) is included to create those json files: `./collect.py bin/ --url 'https://downloads.openwrt.org/releases/{release}/targets/{target}' > names-test.json`.

Note: Files `names-18.06.7.json` and `names-19.07.1.json` contain data for older OpenWrt releases that do not support JSON output. It was generated using heuristics.

## Contributions

It would be nice to have more features. E.g.:

* more translations
* help text for images
* better CSS

## Similar Projects

- [Gluon Firmware Selector](https://github.com/freifunk-darmstadt/gluon-firmware-selector): Original source of this project for images generated by [Gluon](https://github.com/freifunk-gluon/), now with pictures.
- [Freifunk Hennef Firmware Downloader](https://github.com/Freifunk-Hennef/ffhef-fw-dl): Similar to the project above, but PHP based.
- [LibreMesh Chef](https://chef.libremesh.org/): Allows to select configurations.
- [GSoC Firmware Selector](https://github.com/sudhanshu16/openwrt-firmware-selector/): Result of the GSoC
- [FFB Firmware Selector](https://github.com/freifunk-bielefeld/firmware-selector): Build for Freifunk Bielefeld

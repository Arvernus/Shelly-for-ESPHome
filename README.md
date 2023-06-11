# Shelly for ESPHome

This Project is supposes to provide a simple and intuitive way to flash a Shelly Device with ESPHome. The easiest way to use this tool is to go to the [Installer Page](https://arvernus.github.io/Shelly-for-ESPHome/). There one can choose between direct installation in the browser via cable or via OTA update directly from the stock firmware.

## Warnings

The process of flashing a device OTA may fail and leave the device in an unknown status.

## Participate in the Project

There is a [Github-Action](.github/workflows/CI.yml)  that builds firmware's for all `.yaml` at `/`. Additional yaml's for other devices may be added.

All `.yaml` files may be buildable ESPHome config files and at least contain tho following config entry's:

```yaml
substitutions:
  devicename: "shelly-1" # The Name of the Device following the rules defined at https://esphome.io/components/esphome.html
  devicename_h: "Shelly 1" # The Name of the Device in an humanly readable form.

esphome:
    name_add_mac_suffix: true
```
ToDo: APiv2
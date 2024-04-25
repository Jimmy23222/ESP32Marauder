# Load
Load your current list of SSIDs or Access Points. If you saved a list of SSIDs for beacons or you have scanned access points, you can load these items from your SD card. The loaded items will populate your SSID or access point lists respectively.

**Note:** Because of ArduinoJson limitations, there is a limit to how many APs can be loaded from your SD files and it is around ~20 depending on your current memory usage. We are currently working on workarounds.

## Menu Path
`WiFi`>`General`>`Save/Load Files`

## CLI
This function is available for use via the [Marauder CLI](cli). The following documentation describes command usage.

### Usage
`load -a/-s`

#### Arguments
| Argument | Required/Optional | Description |
| -------- | ----------------- | ----------- |
| `-s` | Optional | Save list of SSIDs |
| `-a` | Optional | Save list of Access Points |
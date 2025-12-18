# generate_os_list

The script resolves the latest RaspAP release version and date, extracts the images and uses `shasum()` to compute SHA values.
The resulting output is written to a JSON file in a format expected by the [RPi Imager](https://github.com/raspberrypi/rpi-imager).

## Usage

1. Clone this repository: `git clone https://github.com/billz/generate_os_list.git`
2. Enter the working directory: `cd generate_os_list`
3. Download the arm64 and armhf compressed archives from the [latest releases](https://github.com/RaspAP/raspap-webgui/releases/latest)
4. Execute the script with `./generate_os_list.sh` or `bash ./generate_os_list.sh`

## Example output

```
 ./generate_os_list.sh
Fetching latest release from GitHub...
Found release: 3.5.0 (published: 2025-12-01)
Generated os-sublist-raspap.json
{
  "name": "RaspAP",
  "description": "The easiest, full-featured wireless router for Debian-based devices.",
  "icon": "https://raspap.com/assets/images/raspAP-logo.svg",
  "random": false,
  "subitems": [
    {
      "name": "RaspAP 32-bit (armhf)",
      "description": "The easiest, full-featured wireless router for Debian-based devices.",
      "icon": "https://raspap.com/assets/images/raspAP-logo.svg",
      "url": "https://github.com/RaspAP/raspap-webgui/releases/download/3.5.0/raspap-trixie-armhf-lite-3.5.0.img.zip",
      "extract_size": 3137339392,
      "extract_sha256": "ac993d39ea94ad71d72f23abb17dcebbbddab5eafb98244737d2d86ab2d05011",
      "image_download_size": 901768702,
      "image_download_sha256": "bc560b4cfb06656441ea3179b39dfef7ee4a30cb68e299a4e0d8f002df74642d",
      "release_date": "2025-12-01",
      "init_format": "systemd",
      "devices": [
        "pi5-32bit",
        "pi4-32bit",
        "pi3-32bit",
        "pi2-32bit"
      ],
      "capabilities": []
    },
    {
      "name": "RaspAP 64-bit (arm64)",
      "description": "The easiest, full-featured wireless router for Debian-based devices.",
      "icon": "https://raspap.com/assets/images/raspAP-logo.svg",
      "url": "https://github.com/RaspAP/raspap-webgui/releases/download/3.5.0/raspap-trixie-arm64-lite-3.5.0.img.zip",
      "extract_size": 3472883712,
      "extract_sha256": "fda70f5b74d262d049b984701409afefe33fa1cf41d2bbe90578b125cb8f7021",
      "image_download_size": 930083318,
      "image_download_sha256": "c8d247cae7837a6ad6d0b3173df1feb87253c6f9e18973e05fb2523f392785a4",
      "release_date": "2025-12-01",
      "init_format": "systemd",
      "devices": [
        "pi5-64bit",
        "pi4-64bit",
        "pi3-64bit"
      ],
      "capabilities": []
    }
  ]
}
```

# Ubiquiti Unifi Configs
Configuration file samples for the Ubiquiti Unifi series of products.

These documents are samples for various Ubiquiti Unifi products. I've created them to help new users with the Ubiquiti Unifi products. Please submit updates and changes. Patches are welcome. There are no comments in any of the files as comments are not supported in JSON. Please see the descriptions below. Using the CLI of the various devices and some Google searching for available commands can help as well.

## USG Samples

For USG, the JSON files are placed in the site data directory of the controller. On the Unifi Cloud Key controller, the directory is usually **/usr/lib/unifi/data/sites/default**

The file must always be called **config.gateway.json** and there is only one file. Multiple JSON files have to be combined in order to use more than one configuration snippet.

_NOTE_ : If the config.gateway.json file has errors, the USG could go into a reboot loop. If that happens, fix the JSON file and restart the controller. When the USG reboots, it should be fine.

### Documents

- Products/USG/upnp_config.gateway.json
  - _Enable UPnP / NAT-PMP on the USG_



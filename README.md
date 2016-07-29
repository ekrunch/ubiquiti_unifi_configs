# Ubiquiti Unifi Configs
Configuration file samples for the Ubiquiti Unifi series of products.

These documents are samples for various Ubiquiti Unifi products. I've created them to help new users with the Ubiquiti Unifi products. Please submit updates and changes. Patches are welcome. There are no comments in any of the files as comments are not supported in JSON. Please see the descriptions below. Using the CLI of the various devices and some Google searching for available commands can help as well.

## Products

- Ubiquiti Universal Security Gateway %28USG%29 - [Sample Files](https://github.com/ekrunch/ubiquiti_unifi_configs/tree/master/Products/USG)

## USG Samples

For USG, the JSON files are placed in the site data directory of the controller. On the Unifi Cloud Key controller, the directory is usually **/usr/lib/unifi/data/sites/default**

The file must always be called **config.gateway.json** and there is only one file allowed. Multiple JSON files have to be combined in order to use more than one configuration snippet. There is a "combined" sample in the repository that covers what it could look like with multiple services edited.

_NOTE_ : If the config.gateway.json file has errors, the USG could go into a reboot loop. If that happens, fix the JSON file and restart the controller. When the USG reboots, it should be fine.

### Additional Links

- Unifi controller config.properties file (Affects all Unifi components attached to the controller)
  - <https://help.ubnt.com/hc/en-us/articles/205146040-UniFi-config-properties-File-Explanation>
- More discussion around the config.gateway.json file (Affects USG devices attached to the controller)
  - <https://help.ubnt.com/hc/en-us/articles/215458888-UniFi-How-to-further-customize-USG-configuration-with-config-gateway-json>
- If you use a Cloud Key and want to manually change the firmware version (to run betas and such), this link explains how it's done.
  - <https://help.ubnt.com/hc/en-us/articles/216655518-UniFi-How-to-manually-change-the-controller-version-on-Cloud-Key-via-SSH>


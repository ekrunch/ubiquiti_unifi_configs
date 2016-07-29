## USG Samples

For USG, the JSON files are placed in the site data directory of the controller. On the Unifi Cloud Key controller, the directory is usually **/usr/lib/unifi/data/sites/default**

The file must always be called **config.gateway.json** and there is only one file allowed. Multiple JSON files have to be combined in order to use more than one configuration snippet. There is a "combined" sample in the repository that covers what it could look like with multiple services edited.

_NOTE_ : If the config.gateway.json file has errors, the USG could go into a reboot loop. If that happens, fix the JSON file and restart the controller. When the USG reboots, it should be fine.

### Current Versions
All tests listed below were performed on the following firmware
USG : v4.3.17 (Currently beta as of 2016/07/27)
Controller : 5.1.1 (Currently beta as of 2016/07/27)

### Documents

- [upnp_config.gateway.json](https://github.com/ekrunch/ubiquiti_unifi_configs/blob/master/Products/USG/upnp_config.gateway.json)
  - _Enable UPnP / NAT-PMP on the USG_ - **Working**
- [dnscache_config.gateway.json](https://github.com/ekrunch/ubiquiti_unifi_configs/blob/master/Products/USG/dnscache_config.gateway.json)
  - _Increase DNS Cache size_ - **Working** - _Requires USG 4.3.17 / Controller 5.1.1_ 
- [static_dns_entry_config.gateway.json](https://github.com/ekrunch/ubiquiti_unifi_configs/blob/master/Products/USG/static_dns_entry_config.gateway.json) 
  - _Create static entries in the DNS server_ - **Testing** - Recent fixes in this area that could solve the problem.
- [dnsdomainname_config.gateway.json](https://github.com/ekrunch/ubiquiti_unifi_configs/blob/master/Products/USG/dnsdomainname_config.gateway.json)
  - _Set domain name properly_ - **Working**
- [ntp_config.gateway.json](https://github.com/ekrunch/ubiquiti_unifi_configs/blob/master/Products/USG/ntp_config.gateway.json)
  - _Set NTP Servers_ - **Working**
- [combined_config.gateway.json](https://github.com/ekrunch/ubiquiti_unifi_configs/blob/master/Products/USG/combined_config.gateway.json)
  - _Combination of several files, to illustrate how it works_ - **Working** - _Requires USG 4.3.17 / Controller 5.1.1_

### Reference Documentation

- The USG is built on Ubiquiti's EdgeOS, which is based on Vyatta Core. To the best of my knowledge, it was forked from Vyatta Core 6.3, so I have put up the [Vyatta 6.3 documentation](https://github.com/ekrunch/ubiquiti_unifi_configs/tree/master/Reference%20Documentation/Vyatta/6.3) as well. 

### Additional Links

- Unifi controller config.properties file (Affects all Unifi components attached to the controller)
  - <https://help.ubnt.com/hc/en-us/articles/205146040-UniFi-config-properties-File-Explanation>
- More discussion around the config.gateway.json file (Affects USG devices attached to the controller)
  - <https://help.ubnt.com/hc/en-us/articles/215458888-UniFi-How-to-further-customize-USG-configuration-with-config-gateway-json>
- If you use a Cloud Key and want to manually change the firmware version (to run betas and such), this link explains how it's done.
  - <https://help.ubnt.com/hc/en-us/articles/216655518-UniFi-How-to-manually-change-the-controller-version-on-Cloud-Key-via-SSH>


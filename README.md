# Ubiquiti Unifi Configs
Configuration file samples for the Ubiquiti Unifi series of products.

These documents are samples for various Ubiquiti Unifi products. I've created them to help new users with the Ubiquiti Unifi products. Please submit updates and changes. Patches are welcome. There are no comments in any of the files as comments are not supported in JSON. Please see the descriptions below. Using the CLI of the various devices and some Google searching for available commands can help as well.

## USG Samples

For USG, the JSON files are placed in the site data directory of the controller. On the Unifi Cloud Key controller, the directory is usually **/usr/lib/unifi/data/sites/default**

The file must always be called **config.gateway.json** and there is only one file allowed. Multiple JSON files have to be combined in order to use more than one configuration snippet. There is a "combined" sample in the repository that covers what it could look like with multiple services edited.

_NOTE_ : If the config.gateway.json file has errors, the USG could go into a reboot loop. If that happens, fix the JSON file and restart the controller. When the USG reboots, it should be fine.

### Documents

All files are located in *Products/USG*

- upnp_config.gateway.json
  - _Enable UPnP / NAT-PMP on the USG_ - **Working**
- dnscache_config.gateway.json
  - _Increase DNS Cache size_ - **Not Working** - Ubiquiti said this is a known issue. Another process overwrites the DNS cache and host entries settings. Supposedly this will be fixed somtime soon.
- static_dns_entry_config.gateway.json 
  - _Create static entries in the DNS server_ - **Not Working** - Same reason as above file. There's a workaround using the static host commands that I _think_ is working. In testing...
- dnsdomainname_config.gateway.json 
  - _Set domain name properly_ - **Working**
- combined_config.gateway.json
  - _Combination of several files, to illustrate how it works_ -**Testing**

### Reference Documentation

- The USG is built on Ubiquiti's EdgeOS, which is based on Vyatta Core. To the best of my knowledge, it was forked from Vyatta Core 6.3, so I have put up the Vyatta 6.3 documentation as well. 


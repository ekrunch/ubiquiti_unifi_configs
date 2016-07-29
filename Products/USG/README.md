## USG Samples

For USG, the JSON files are placed in the site data directory of the controller. On the Unifi Cloud Key controller, the directory is usually **/usr/lib/unifi/data/sites/default**

The file must always be called **config.gateway.json** and there is only one file allowed. Multiple JSON files have to be combined in order to use more than one configuration snippet. There is a "combined" sample in the repository that covers what it could look like with multiple services edited.

_NOTE_ : If the config.gateway.json file has errors, the USG could go into a reboot loop. If that happens, fix the JSON file and restart the controller. When the USG reboots, it should be fine. I highly recommend the use of a JSON validator before applying to your gateway. Search for **JSON Validator** or **JSON Lint** to find one. Using a text editor with syntax highlighting helps a lot as well.

### Current Versions
All tests listed below were performed on the following firmware
USG : v4.3.17 (Currently beta as of 2016/07/27)
Controller : 5.1.1 (Currently beta as of 2016/07/27)

### Documents

| Filename | Description | Status | Notes |
| :------- | :---------- | :----: | :---- |
| combined_config.gateway.json | Combination of several files, to illustrate how it works | **Working** ||
| dhcp_domain_name_config.gateway.json | Combination of several files, to illustrate how it works | **Working** ||
| dnscache_config.gateway.json | Increase DNS Cache size | **Working** | Requires USG 4.3.17 / Controller 5.1.1 |
| dnsdomainname_config.gateway.json | Set USG domain name properly | **Working** ||
| ipv6_comcast_config.gateway.json | Experimental IPv6 Configuration for use in residental setups. Currently uses DHCPv6-PD and works with Comcast | **Testing** ||
| ntp_config.gateway.json	| Set NTP Servers | **Working** ||
| ssh_key_config.gateway.json |	Set SSH Key for logging in without a password | **Testing** | It is highly recommended that you use the "loadkey" command from the USG and then view the resulting configuration to understand the structure here. This one isn't something you'll want to type in manually. |
| static_dns_entry_config.gateway.json | Create static entries in the DNS server | **Testing** | Recent fixes in this area that could solve the problem. |
| upnp_config.gateway.json | Enable UPnP / NAT-PMP on the USG | **Working** ||

### Reference Documentation

- The USG is built on Ubiquiti's EdgeOS, which is based on Vyatta Core. To the best of my knowledge, it was forked from Vyatta Core 6.3, so I have put up the [Vyatta 6.3 documentation](https://github.com/ekrunch/ubiquiti_unifi_configs/tree/master/Reference%20Documentation/Vyatta/6.3) as well. 

### Additional Links

- More discussion around the config.gateway.json file (Affects USG devices attached to the controller)
  - <https://help.ubnt.com/hc/en-us/articles/215458888-UniFi-How-to-further-customize-USG-configuration-with-config-gateway-json>


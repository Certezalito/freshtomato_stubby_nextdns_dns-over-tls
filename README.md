Stubby opportunistic dns-over-tls (DoT) configuration for NextDNS on FreshTomato

Requires Stubby enabled on Advanced > DHCP/DNS tab, Requires your NextDNS cpe ID

Within FreshTomato, paste this script into Administration > Scripts > WAN Up (main), on reboot the script will take effect.
Optionally paste the script into shell prompt for immediate results, however the configuration will be lost during the reboot unless its saved in the scripts section of FreshTomato

Test settings @ https://test.nextdns.io/, it should show ""protocol": "DOT""
Replace cpe with your particular cpe ID from NextDNS, replace devicename with your choosing
To revert your stubby changes:
'rm /etc/stubby/stubby_alt.yml && service stubby restart'

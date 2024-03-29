# Stubby dns-over-tls (DoT) configuration for NextDNS on FreshTomato

## Requirements:
* "Use Stubby" enabled on "Advanced" > "DHCP/DNS" tab
* Your NextDNS cpe ID (https://my.nextdns.io/ see "ID")

## Directions:
Replace `cpe` with your particular cpe ID from NextDNS

Replace `devicename` with your choosing

For Strict Privacy set `mode=strict` else set mode to anything for opportunistic mode

Paste this script into Administration > Scripts > WAN Up (main) and during reboot the script will take effect

Optionally paste the script into shell prompt for immediate results, however the configuration will be lost on reboot unless its saved in the scripts section of FreshTomato

## Testing:
Disable any browser specific nextdns settings

Visit https://test.nextdns.io/ and it should show `"protocol": "DOT",`   

## Revert changes:
`rm /etc/stubby/stubby_alt.yml && service stubby restart`

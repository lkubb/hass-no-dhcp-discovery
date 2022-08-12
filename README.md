# Disable DHCP Autodiscovery
## General
Installing this custom component disables DHCP autodiscovery by overriding the core integration. It lets you keep `default_config` in your configuration and thus keeps you from managing all those by hand.

## Motivation
I want to run my containers rootless inside Podman. DHCP autodiscovery requires `cap_net_raw` capability, which can be quite insecure. This would not be a problem, in itself, but in addition my PiHole logs show that HA spams PTR requests every hour. This is caused by the DHCP integration as well.

## References
* https://github.com/Hypfer/home-assistant-no-cloud-custom-component

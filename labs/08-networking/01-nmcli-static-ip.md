# Lab 01: Configure a Static IPv4 Address with nmcli

## Objective

Configure a static IPv4 address using NetworkManager and verify connectivity.

## RHCSA Skills Covered

- Configure IPv4 networking
- Configure a default gateway
- Configure DNS servers
- Manage connections with nmcli
- Verify network configuration

## Scenario

A newly deployed server requires a persistent network configuration.

Apply the following settings:

| Setting | Value |
|----------|----------|
| Interface | ens18 |
| IPv4 Address | 10.2.0.230/24 |
| Gateway | 10.2.0.1 |
| DNS Server | 10.1.0.2, 8.8.8.8 |

The configuration must survive a reboot.

## Environment Discovery

Identify interfaces:

```
nmcli device status
```

## Add IPv4 IP details
```
nmcli connection modify ens18 \
  ipv4.address 10.2.0.231/24 \
  ipv4.gateway 10.2.0.1 \
  ipv4.dns "10.1.0.2 8.8.8.8" \
  ipv4.method manual
```
## Check the interfaces
nmcli connection show ens18
nmcli connection show
```

## Now restart the interface
```
nmcli connection down ens18
nmcli connection show 
nmcli connection up ens18
nmcli connection show
```

## Check and confirm the interface is up and has the correct information
```
ip address
ip route
nmcli device show ens18 | grep DNS
```

Then reboot and confirm that the new configuration survives a reboot.


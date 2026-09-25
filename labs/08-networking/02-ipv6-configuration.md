# Lab 02: Configure an IPv6 Address Using nmcli

## Objective

Configure a static IPv6 address using NetworkManager and verify that the configuration survives a system reboot.

RHCSA skills covered:

- Configure IPv6 networking
- Configure an IPv6 gateway
- Manage network connections using `nmcli`
- Verify IPv6 connectivity
- Verify persistent network configuration

---

## Scenario

A server requires IPv6 connectivity on the management network.

Configure the following settings:

| Setting | Value |
|----------|----------|
| Interface | ens160 |
| IPv6 Address | 2001:db8:1::50/64 |
| Gateway | 2001:db8:1::1 |

The configuration must persist after reboot.

---

## Environment Discovery

Display available interfaces:

```bash
ip link show
```

Display active connections:

```bash
nmcli connection show
```

Verify existing IPv6 configuration:

```bash
ip -6 addr show
```

---

## Configuration

Configure the IPv6 address:

```bash
nmcli connection modify ens160 \
  ipv6.addresses 2001:db8:1::50/64 \
  ipv6.gateway 2001:db8:1::1 \
  ipv6.method manual
```

Apply the configuration:

```bash
nmcli connection up ens160
```

---

## Verification

Display IPv6 addressing:

```bash
ip -6 addr show ens160
```

Expected output:

```text
inet6 2001:db8:1::50/64
```

Display IPv6 routes:

```bash
ip -6 route
```

Expected output:

```text
default via 2001:db8:1::1
```

---

## Connectivity Tests

Test the gateway:

```bash
ping6 -c 4 2001:db8:1::1
```

Test another IPv6 host:

```bash
ping6 -c 4 2001:4860:4860::8888
```

Verify name resolution using IPv6:

```bash
ping6 -c 4 google.com
```

---

## Viewing IPv6 Configuration

Display connection details:

```bash
nmcli connection show ens160
```

Display all IPv6 information:

```bash
ip -6 addr
```

Display IPv6 routes:

```bash
ip -6 route
```

---

## Persistence Testing

Reboot the system:

```bash
reboot
```

After logging back in:

```bash
ip -6 addr show
ip -6 route
```

Verify the IPv6 address and default route remain configured.

---

## Troubleshooting

### IPv6 Address Missing

Check connection status:

```bash
nmcli connection show --active
```

Bring the connection online:

```bash
nmcli connection up ens160
```

---

### No Default Route

Check IPv6 routes:

```bash
ip -6 route
```

Review connection settings:

```bash
nmcli connection show ens160
```

---

### Unable to Reach Remote IPv6 Hosts

Verify local address:

```bash
ip -6 addr
```

Verify default route:

```bash
ip -6 route
```

Ping the configured gateway:

```bash
ping6 -c 4 2001:db8:1::1
```

---

## RHCSA Exam Notes

Useful commands:

```bash
ip -6 addr

ip -6 route

nmcli connection show

nmcli connection modify

nmcli connection up
```

Remember:

- Most RHCSA candidates are stronger with IPv4 than IPv6.
- IPv6 tasks are often easy marks if you've practised them.
- Always verify both address assignment and routing.
- Ensure configuration survives a reboot.

---

## Lessons Learned

| Date | Notes |
|--------|--------|
| YYYY-MM-DD | Add observations and troubleshooting notes here |

---

## Completion Checklist

- [x] Interface identified
- [ ] IPv6 address configured
- [ ] IPv6 gateway configured
- [ ] Connectivity verified
- [ ] Routing verified
- [ ] Reboot test passed
- [ ] Lessons learned updated

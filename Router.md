# Basic Cisco Router Configuration Checklist

## Initial Setup:
- `enable` (enter privileged EXEC mode)
- `configure terminal` (enter global configuration mode)
- `hostname [hostname]` (set the hostname)
- `banner motd [banner message]` (set MOTD banner)
- `enable secret [password]` (set enable secret password)
- `line console 0` 
  - `password [password]` 
  - `login` (set console password)
- `line vty 0 15` 
  - `password [password]` 
  - `login` (set Telnet/SSH password)
- `service password-encryption` (encrypt passwords)

## Password Encryption:
- `service password-encryption` (enable password encryption)

## Interface Configuration:
- `interface [interface]` 
  - `ip address [ip address] [subnet mask]` (configure IP address)
- `interface [interface]` 
  - `description [description]` (set interface description)

## DHCP Configuration:
- `ip dhcp excluded-address [start IP] [end IP]`
- `ip dhcp pool [pool name]` 
  - `network [network] [subnet mask]` (configure DHCP pool)
  - `default-router [default gateway]` (set default gateway)
  - `dns-server [DNS server]` (set DNS server)


# Basic Cisco Router Configuration Checklist

## Initial Setup (Executed from privileged EXEC mode):
- [ ] `enable` (enter privileged EXEC mode)
- [ ] `configure terminal` (enter global configuration mode)
- [ ] `hostname [hostname]` 
- [ ] `banner motd [banner message]`
- [ ] `enable secret [password]` 
- [ ] `line console 0` 
  - [ ] `password [password]` 
  - [ ] `login` (set console password)
- [ ] `line vty 0 15` 
  - [ ] `password [password]` 
  - [ ] `login` (set Telnet/SSH password)
- [ ] `service password-encryption` (encrypt passwords)

## Password Encryption (Executed from global configuration mode):
- [ ] `service password-encryption` (enable password encryption)

## Interface Configuration (Executed from global configuration mode):
- [ ] `interface [interface]` 
  - [ ] `ip address [ip address] [subnet mask]` 
  - [ ] `description [description]` (set interface description)

## DHCP Configuration (Executed from global configuration mode):
- [ ] `ip dhcp excluded-address [start IP] [end IP]`
- [ ] `ip dhcp pool [pool name]` 
  - [ ] `network [network] [subnet mask]` 
  - [ ] `default-router [default gateway]` 
  - [ ] `dns-server [DNS server]` 


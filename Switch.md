# Basic Cisco Switch Configuration Checklist

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

## VLAN Configuration (Executed from global configuration mode):
- [ ] `vlan [vlan_number]` (create VLAN)
- [ ] `name [vlan_name]` (assign VLAN name)

## Interface Configuration (Executed from global configuration mode):
- [ ] `interface [interface]` 
  - [ ] `switchport mode access` (set interface to access mode)
  - [ ] `switchport access vlan [vlan_number]` (assign VLAN to interface)

## Trunk Configuration (Executed from global configuration mode):
- [ ] `interface [interface]` 
  - [ ] `switchport mode trunk` (set interface to trunk mode)
  - [ ] `switchport trunk allowed vlan [vlan_list]` (specify allowed VLANs on trunk)
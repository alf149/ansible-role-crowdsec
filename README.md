# Crowdsec
=========

This Ansibel roles installs Crowdsec incl. hub, collections, scenarios, postoverflows, parsers, bouncers and prometheus endpoint.

## Requirements
------------
Tested on:
  platforms:
      - name: Ubuntu
        versions:
          - bionic  #16.04
          - focal   #20.04
          - impish  #21.10
      - name: Debian
        versions:
          - bookworm # 11
          - bullseye # 10
      
      - name: EL
        versions:
          - '8'   #Rocky & alma Linux og Oracle Linux
          - '7'   #Oracle Linux

## Role Variables
--------------
Available variables with default values (see `defaults/main.yml`):

## Dependencies
------------
None

## Example Playbook
----------------
```yaml
- hosts: all

  vars:
    ban_duration: "duration: 4h" # PROD eg. 10m for testing

  roles:
    - alf149.crowdsec 
```

## TODO
------
- Test on Windows server when crowdsec makes a signed version. 
- Maby autodetect nftables/iptables and load the correct bouncer. 

## License
-------
MiT

## Author Information
------------------
Alf149

## Error reporting. 
------------------
Use github issues or make at PR. 

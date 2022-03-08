# Crowdsec
=========

This Ansibel roles installs Crowdsec incl. hub, collections, scenarios, postoverflows, parsers, bouncers and prometheus endpoint.

## Requirements
------------
Tested on Ubuntu 20.04 LTS server but should work on other (supported) versions of Ubuntu as well as other Debian derivates.

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
- Test on more Debian based distros 
- Test on Redhat based distros 



## License
-------

MiT

## Author Information
------------------

Alf149

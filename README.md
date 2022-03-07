# Crowdsec
=========

Install Crowdsec incl. hub, collections, scenarios, postoverflows, parsers, bouncers and prometheus endpoint.

## Requirements
------------
Testet on Ubuntu 20.04 LTS server

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
    - crowdsec
 
```
## TODO
------
Test on mere Debian based distros 
Test on Redhat based distros 



## License
-------

MiT

## Author Information
------------------

Alf149
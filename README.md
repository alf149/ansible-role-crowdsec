# Crowdsec
This ansible roles installs Crowdsec incl. hub, collections, scenarios, postoverflows, parsers, bouncers and prometheus endpoint.

## Requirements
Ansible master running version 2.12 

Tested on:
```yaml
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
          - '8'   #Rocky & alma Linux and Oracle Linux
          - '7'   #Oracle Linux
```

## how to install.
I use ansible-galaxy do make a requirements.yml
```yaml
roles:
  - geerlingguy.security
  - alf149.crowdsec
```
And run 
`ansible-galaxy install -r requirements.yml` This wil import this role to your ansible projekt. 


## Role Variables
Available variables with default values (see `defaults/main.yml`)
variables can be host specific in group_vars/host.yml

## Example Playbook
```yaml
- hosts: all

  vars:
    cs_ban_duration: "duration: 4h" # PROD eg. 10m for testing

  roles:
    - alf149.crowdsec 
```

## Manual tasks could be handy
ansible HOST -m shell -a "sudo cscli parsers install crowdsecurity/whitelists --force"
ansible 'group' -m shell -a "sudo cscli parsers remove crowdsecurity/whitelists --force"
ansible 'group' -m shell -a "sudo systemctl reload crowdsec"

## TODO
- Test on Windows server  
- Maby autodetect nftables/iptables and load the correct bouncer. 

## Error reporting. 
Use github issues or make a PR. 

## Author Information
------------------

[Alf149](https://github.com/alf149) 

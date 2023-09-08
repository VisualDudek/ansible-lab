

## Discussion

**AWS lab** how to "auto-yes" for fingerprints when first time running playbook on new ec2 instances?
Temporary solution:
editing: `/etc/ansible/ansible.cfg` or `~/.ansible.cfg`:
```txt
[defaults]
host_key_checking = False
```
TODO: further investigation
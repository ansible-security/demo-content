# Check Point Ansible Examples
This repo contains examples using Ansible for Check Point

## Ansible Module Examples

### Configuring an Host Object with Check Point(CP)

```yaml
    - name: Create host object
      cp_mgmt_host:
        color: dark green
        ipv4_address: 192.0.2.2
        name: New CP_MGMT Host 1
        state: present
        auto_publish_session: true
```


### Get the Host facts

```yaml
    - name: Collect-host facts
      cp_mgmt_host_facts:
        name: New CP_MGMT Host 1
      register: cp_host
    - name: Display host facts
      debug:
        msg: "{{ cp_host }}"
```

The full sample playbooks can be found here: [Checkpoint Plays](https://github.com/ansible-security/ansible-security-playbooks/tree/master/playbooks/checkpoint)

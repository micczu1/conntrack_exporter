**Moved to: https://github.com/micczu1/ansible-conntrack_exporter**

# Ansible Role: conntrack_exporter

## Description

Deploy prometheus [conntrack_exporter](https://github.com/ncabatoff/process-exporter) using Ansible.

## Requirements

- Ansible >= 2.3
- `GLIBCXX_3.4.21' (Centos 7 has glibc-2.17-260.el7_6.4.x86_64)
- `CXXABI_1.3.8'
- libnetfilter-conntrack-dev (Ubuntu/Debian: apt-get install libnetfilter-conntrack-dev)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `conntrack_exporter_version` | 0.3 | conntrack_exporter package version |
| `conntrack_exporter_listen_port` | "9101" | Address on which conntrack_exporter will listen |

## Example

### Playbook

Use it in a playbook as follows:

```yaml
- hosts: all
  become: yes
  roles:
    - conntrack_exporter
```

## Credits

This role is inspired by https://github.com/cloudalchemy/ansible-mysqld-exporter  
conntrack_exporter is created by: https://github.com/hiveco/conntrack_exporter and this is only wrap-up in Ansible role.

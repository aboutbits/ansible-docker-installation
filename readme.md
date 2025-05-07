Ansible Docker Installation Role
================================

Installation of a Docker server.

## Role Variables

- `docker_installation_bridge_ip`: Specifies the IP address and netmask to use for Docker’s default bridge

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-docker-installation
      vars:
        docker_installation_bridge_ip: "172.26.0.1/16"
```

## Versioning

In order to have a versioning in place and working, create leightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag v3
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d v3
git push origin :refs/tags/v3
git tag v3
git push --tags
```

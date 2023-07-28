Ansible Docker Installation Role
================================

Installation of a Docker server.

## Role Variables

- `docker_installation_compose_version`: The version of docker-compose that should be installed
- `docker_installation_bridge_ip`: Specifies the IP address and netmask to use for Docker’s default bridge

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-docker-installation
      vars:
        docker_installation_compose_version: 1.25.4
        docker_installation_bridge_ip: "172.26.0.1/16"
```

## Versioning

In order to have a verioning in place and working, create leightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag 1.0
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d 1.0
git push origin :refs/tags/1.0
git tag 1.0
git push --tags
```

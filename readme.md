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

## Build & Publish

To build and publish the role, visit the GitHub Actions page of the repository and trigger the workflow "Release Package" manually.

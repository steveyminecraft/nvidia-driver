# NVIDIA Driver Ansible Role

This role installs NVIDIA drivers on Devuan, supports 32-bit drivers, and optionally replaces the `nvidia-persistenced` init script.

## Requirements
- Devuan linux
- Ansible 2.9+

## Role Variables
```yaml
replace_nvidia_persistenced: false
require_32bit_support: false
```

## Example Playbook
```yaml
- hosts: gpu_servers
  roles:
    - role: nvidia_driver
      vars:
        replace_nvidia_persistenced: true
        require_32bit_support: true
```

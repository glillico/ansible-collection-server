# Ansible Collection - glillico.server

This collections containes server related roles to help with the setup and configuration of a Linux server.

## Includes
  - [glillico.add_rm_pkgs](https://github.com/glillico/ansible-role-add_rm_pkgs) 
  - [glillico.auto_pkg_updates](https://github.com/glillico/ansible-role-auto_pkg_updates)
  - [glillico.configure_firewall](https://github.com/glillico/ansible-role-configure_firewall)
  - [glillico.configure_ntp](https://github.com/glillico/ansible-role-configure_ntp)
  - [glillico.configure_sshd](https://github.com/glillico/ansible-role-configure_sshd)
  - [glillico.configure_sudo](https://github.com/glillico/ansible-role-configure_sudo)
  - [glillico.copy_etc_issue](https://github.com/glillico/ansible-role-copy_etc_issue)
  - [glillico.deploy_firewall](https://github.com/glillico/ansible-role-deploy_firewall)
  - [glillico.install_docker](https://github.com/glillico/ansible-role-install_docker)
  - [glillico.install_fail2ban](https://github.com/glillico/ansible-role-install_fail2ban)
  - [glillico.install_figurine](https://github.com/glillico/ansible-role-install_figurine)
  - [glillico.manage_selinux](https://github.com/glillico/ansible-role-manage_selinux)
  - [glillico.reboot_server](https://github.com/glillico/ansible-role-reboot_server)
  - [glillico.regenerate_ssh_host_keys](https://github.com/glillico/ansible-role-regenerate_ssh_host_keys)
  - [glillico.set_hostname](https://github.com/glillico/ansible-role-set_hostname)
  - [glillico.setup_ssh_keys](https://github.com/glillico/ansible-role-setup_ssh_keys)
  - [glillico.setup_users](https://github.com/glillico/ansible-role-setup_users)
  - [glillico.sync_sudo](https://github.com/glillico/ansible-role-sync_sudo)
  - [glillico.update_pkgs](https://github.com/glillico/ansible-role-update_pkgs)

# Usage

This collection can be installed locally using the ansible-galaxy command.

`ansible-galaxy collection install glillico.server`

Or you can include this collection in your ansible playbook's requirements.yml file:

```
---
- hosts: all

  collections:
    - glillico.server

  roles:
    - glillico.server.add_rm_pkgs
    - glillico.server.copy_etc_issue
    - role: glillico.server.deploy_firewall
      vars:
        dpfw_firewalld_rules:
          - dpfw_firewalld_state: 'enabled'
            dpfw_firewalld_port: '8080/tcp'
            dpfw_firewalld_zone: 'public'
```

## License

MIT

## Author Information

Created in 2024 by Graham Lillico.
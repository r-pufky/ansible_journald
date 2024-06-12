# Journald
Manage journald configuration.

## Requirements
[supported platforms](https://github.com/r-pufky/ansible_journald/blob/main/meta/main.yml)

## Role Variables
[defaults](https://github.com/r-pufky/ansible_journald/blob/main/defaults/main.yml)

## Dependencies
N/A

## Example Playbook
Lightweight management of journald.

Set journald to log only to memory, limiting size to 200MB.

host_vars/client.example.com/vars/journald.yml
``` yaml
journald_storage: 'volatile'
journald_system_max_use: '200M'
journald_runtime_max_use: '200M'
```

Apply the role
``` yaml
- name: 'Manage journald'
  ansible.builtin.include_role:
    name: 'r_pufky.srv.journald'
```

## Unit Testing
Test framework requires molecule and rootless podman setup.

Run all unit tests:
``` bash
molecule test --all
```

## Issues
Create a bug and provide as much information as possible.

Associate pull requests with a submitted bug.

## License
[AGPL-3.0 License](https://www.tldrlegal.com/license/gnu-affero-general-public-license-v3-agpl-3-0)
 [(direct link)](https://github.com/r-pufky/ansible_users/blob/main/LICENSE)

## Author Information
PGP Fingerprint: [466EEC2B67516C7117C85CE3A0BC35D16698BAB9](https://keys.openpgp.org/vks/v1/by-fingerprint/466EEC2B67516C7117C85CE3A0BC35D16698BAB9)
| [github gist](https://gist.github.com/r-pufky/a8df36977c55b5bb20829267c4c49d22)

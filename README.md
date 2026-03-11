# Journald
Manage journald configuration.

## [Requirements][i]
Requires [r_pufky.deb][g] galaxy-ng collection.

## Role Variables
Detailed variable use documented in defaults. See usage for role operation.

* [defaults][j] - User configurable options.

## Usage

### Example Playbooks

``` yaml
- name: 'Set journald to log only to memory, limiting size to 200MB.'
  ansible.builtin.include_role:
    name: 'r_pufky.deb.journald'
  vars:
    journald_cfg_storage: 'volatile'
    journald_cfg_system_max_use: '200M'
    journald_cfg_runtime_max_use: '200M'
```

## Development
Configure [environment][a].

``` bash
# Run all tests.
molecule test --all
```

### [Releases][b]

 Release | Debian | Ansible | Notes
---------|--------|---------|-------
 3.x.x   | 13     | 2.20    | Ansible 2.20, semantic versioning.
 2.x.x   | 13     | 2.18    | Migrate to Debian Trixie.
 1.x.x   | 12     | 2.18    | Use standardized libraries.
 0.x.x   | 12     | 2.18    | Migration from private repository.

### Issues
Create a bug and provide as much information as possible.

Associate pull requests with a submitted bug.

## License
[AGPL-3.0 License][c] | [direct link][f]

## Author Information
PGP: [466EEC2B67516C7117C85CE3A0BC35D16698BAB9][d] | [github gist][e]


[a]: https://r-pufky.github.io/ansible_docs
[b]: https://semver.org/spec/v2.0.0
[c]: https://www.tldrlegal.com/license/gnu-affero-general-public-license-v3-agpl-3-0
[d]: https://keys.openpgp.org/vks/v1/by-fingerprint/466EEC2B67516C7117C85CE3A0BC35D16698BAB9
[e]: https://gist.github.com/r-pufky/a8df36977c55b5bb20829267c4c49d22

[f]: https://github.com/r-pufky/ansible_journald/blob/main/LICENSE
[g]: https://github.com/r-pufky/ansible_collection_deb
[i]: https://github.com/r-pufky/ansible_journald/blob/main/meta/main.yml
[j]: https://github.com/r-pufky/ansible_journald/tree/main/defaults/main/main.yml
# Ansible Role: local_administrators

[![Build Status](https://img.shields.io/travis/sbaerlocher/ansible.local_administrators.svg?branch=master&style=popout-square)](https://travis-ci.org/sbaerlocher/ansible.local_administrators) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-local_administrators-blue.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/local_administrators) [![Ansible Role](https://img.shields.io/ansible/role/d/id.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/local_administrators)

## Description

Ansible role that adds and removes users and groups to the Local Administraotren group.

## Installation

```bash
ansible-galaxy install sbaerlocher.local_administrators
```

## Requirements

## Role Variables

### local administrators list

A list of users or groups that Local Administrators
should have rights to on the device.

```yml
local_administrators_defaults: []
local_administrators_groups: []
local_administrators_hosts: []
```

#### example local administrators list

```yml
local_administrators_defaults:
  - UserX
  - GroupX
```

### Pure Option

If the state is enable, only the specified elements exist,
and all other unspecified existing elements are removed.

```yml
local_administrators_pure_enable: false
```

### local administrators group

Name of the local administrators group like e.g.
English Administrators or German Administratoren

```yml
local_administrators_group: Administrators
```

## Dependencies

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.local_administrators
```

## Changelog

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2019, Simon Bärlocher

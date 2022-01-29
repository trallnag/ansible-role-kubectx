[![primary](https://github.com/trallnag/ansible-role-kubectx/actions/workflows/primary.yaml/badge.svg)](https://github.com/trallnag/ansible-role-kubectx/actions/workflows/primary.yaml)
[![role](https://img.shields.io/ansible/role/55230)](https://galaxy.ansible.com/trallnag/kubectx)
[![quality](https://img.shields.io/ansible/quality/55230)](https://galaxy.ansible.com/trallnag/kubectx)
[![downloads](https://img.shields.io/ansible/role/d/55230?label=downloads)](https://galaxy.ansible.com/trallnag/kubectx)

# Ansible Role `trallnag.kubectx`

Ansible role that installs the Go version of [`kubectx`](https://github.com/ahmetb/kubectx).

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/kubectx).

## Scope

In:

* Install a single version of kubectx to a global location.

Out:

* Set up tab completion.

## Special Requirements

None.

## Special Dependencies

None.

## Role Variables

Check out [`meta/argument_specs.yaml`](meta/argument_specs.yaml).

## Examples

Here is a minimal Playbook:

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.kubectx
      vars:
        kubectx_version: 0.9.4
        kubectx_arch: x86_64
```

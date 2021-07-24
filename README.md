[![role](https://img.shields.io/ansible/role/55230)](https://galaxy.ansible.com/trallnag/kubectx)
[![quality](https://img.shields.io/ansible/quality/55230)](https://galaxy.ansible.com/trallnag/kubectx)
[![downloads](https://img.shields.io/ansible/role/d/55230?label=downloads)](https://galaxy.ansible.com/trallnag/kubectx)

# Ansible Role `trallnag.kubectx`

Install [kubectx][kubectx] on Linux.

[kubectx]: https://github.com/ahmetb/kubectx

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/kubectx).

## Role Variables

```yaml
kubectx_version:
  default: 0.9.4
  type: str
  required: false
  description: >-
    Version to use. Only 0.9.0 upwards supported. Check here:
    <https://github.com/ahmetb/kubectx/releases>.

kubectx_arch:
  default: x86_64
  type: str
  required: false
  choices: ["x86_64", "arm64", "armhf", "armv7", "ppc64le"]
  description: >-
    Architecture to use.
```

## Example Playbook

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

## Special Requirements

* Linux only.
* Bash completion only.
* `kubectl` must be installed.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag

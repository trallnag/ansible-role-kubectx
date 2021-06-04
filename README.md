[![role](https://img.shields.io/ansible/role/55230)](https://galaxy.ansible.com/trallnag/kubectx)
[![quality](https://img.shields.io/ansible/quality/55230)](https://galaxy.ansible.com/trallnag/kubectx)
[![downloads](https://img.shields.io/ansible/role/d/55230?label=downloads)](https://galaxy.ansible.com/trallnag/kubectx)

# kubectx

Install kubectx on Linux.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/kubectx).

## Role Variables

```yaml
argument_specs:
  main:
    short_description: The main entry point for the "{{ role_name }}" role.
    options:
      kubectx_version:
        type: int
        required: false
        default: 0.9.3
        description: >-
          Version to use. Only 0.9.0 upwards supported.

      kubectx_arch:
        type: str
        required: false
        default: x86_64
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
        kubectx_version: 0.9.3
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

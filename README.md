# Ansible Role: Loris S3Resolver

Installs and configures an [S3Resolver](https://github.com/nmaekawa/hxloris) for the [Loris Image Server](https://github.com/loris-imageserver).

## Requirements

- Ansible 2.0+
- Ubuntu

## Role Variables

| parameter        | required | default                             | comments           |
|------------------|----------|-------------------------------------|--------------------|
| s3resolver_url   | no       | https://github.com/nmaekawa/hxloris | URL to pip install |
| s3resolver_class | no       | hxloris.s3resolver.S3Resolver       | Resolver class     |

## Dependencies

- [ansible-role-loris-imageserver](https://github.com/HUIT-AcademicTechnology-Ops/ansible-role-loris-imageserver)

## Example Playbook

```yml
  ---
  - hosts: server
    remote_user: ubuntu
    become: yes
    roles:
      - ansible-role-loris-imageserver
      - ansible-role-loris-s3resolver
```

## License

MIT/BSD

## Author Information

This role was created in 2020 by Arthur Barrett as a member of the Harvard University IT Academic Technology group.

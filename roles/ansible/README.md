# Ansible Role `jm1.packages.ansible`

This role will install Ansible with support for collections and required tools and libraries e.g. for Ansible modules.

**Tested OS images**
- Cloud image of [`Debian 10 (Buster)` \[`amd64`\]](https://cdimage.debian.org/cdimage/openstack/current/)
- Cloud image of [`Debian 11 (Bullseye)` \[`amd64`\]](https://cdimage.debian.org/images/cloud/bullseye/latest/)
- Ubuntu cloud image of [`Ubuntu 18.04 LTS (Bionic Beaver)` \[`amd64`\]](https://cloud-images.ubuntu.com/bionic/current/)
- Ubuntu cloud image of [`Ubuntu 20.04 LTS (Focal Fossa)` \[`amd64`\]](https://cloud-images.ubuntu.com/focal/)

Available on Ansible Galaxy in Collection [jm1.packages](https://galaxy.ansible.com/jm1/packages).

## Requirements

Module `jm1.pkg.meta_pkg` from Collection [`jm1.pkg`](https://galaxy.ansible.com/jm1/pkg) is used to satisfy all package
dependencies of this Collection [jm1.openstack](https://galaxy.ansible.com/jm1/openstack). To install `jm1.pkg.meta_pkg` you
may follow the steps described in [`README.md`](https://github.com/JM1/ansible-collection-jm1-openstack/blob/master/README.md)
using the provided [`requirements.yml`](https://github.com/JM1/ansible-collection-jm1-openstack/blob/master/requirements.yml).

## Variables

| Name               | Default value                           | Required | Description                                                                                               |
| ------------------ | --------------------------------------- | -------- | --------------------------------------------------------------------------------------------------------- |
| `distribution_id`  | *depends on operating system*           | no       | List which uniquely identifies a distribution release, e.g. `[ 'Debian', '10' ]` for `Debian 10 (Buster)` |

## Dependencies

| Name            | Description                                                                         |
| --------------- | ----------------------------------------------------------------------------------- |
| `jm1.pkg.setup` | Installs necessary software for module `jm1.pkg.meta_pkg` from collection `jm1.pkg` |

## Example Playbook

```yml
- hosts: all
  roles:
  - name: Install Ansible with support for collections and required tools and libraries e.g. for Ansible modules
    role: jm1.packages.ansible
    tags: ["jm1.packages.ansible"]
```

For instructions on how to run Ansible playbooks have look at Ansible's
[Getting Started Guide](https://docs.ansible.com/ansible/latest/network/getting_started/first_playbook.html).

## License

GNU General Public License v3.0 or later

See [LICENSE.md](../../LICENSE.md) to see the full text.

## Author

Jakob Meng
@jm1 ([github](https://github.com/jm1), [galaxy](https://galaxy.ansible.com/jm1), [web](http://www.jakobmeng.de))

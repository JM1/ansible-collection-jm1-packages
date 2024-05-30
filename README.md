# Ansible Collection for Software Deployments

This repo hosts the Ansible collection [`jm1.packages`](https://galaxy.ansible.com/jm1/packages).

The collection includes a variety of Ansible content to help with software deployments.

## Included content

Click on the name of a module or role to view that content's documentation:

- **Roles**:
    * [ansible](roles/ansible/README.md)
    * [git](roles/git/README.md)
    * [libvirt_qemu](roles/libvirt_qemu/README.md)
    * [qemu_guest_agent](roles/qemu_guest_agent/README.md)

## Requirements and Installation

### Installing necessary software

Content in this collection requires additional roles and collections, e.g. to collect operating system facts. You can
fetch them from Ansible Galaxy using the provided [`requirements.yml`](requirements.yml):

```sh
ansible-galaxy collection install --requirements-file requirements.yml
ansible-galaxy role install --role-file requirements.yml
# or
make install-requirements
```

The exact requirements for every module and role are listed in the corresponding documentation.
See the module documentations for the minimal version supported for each module.

### Installing the Collection from Ansible Galaxy

Before using the `jm1.packages` collection, you need to install it with the Ansible Galaxy CLI:

```sh
ansible-galaxy collection install jm1.packages
```

You can also include it in a `requirements.yml` file and install it via
`ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: jm1.packages
    version: 2024.5.30
```

## Usage and Playbooks

You can either call modules and roles by their Fully Qualified Collection Name (FQCN), like `jm1.packages.ansible`, or
you can call modules by their short name if you list the `jm1.packages` collection in the playbook's `collections`,
like so:

```yaml
---
- name: Using jm1.packages collection
  hosts: localhost

  collections:
    - jm1.packages

  roles:
    - name: Install Ansible with support for collections and required tools and libraries e.g. for Ansible modules
      role: ansible
```

For documentation on how to use individual modules and other content included in this collection, please see the links
in the 'Included content' section earlier in this README.

See [Ansible Using collections](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html) for more
details.

## Contributing

There are many ways in which you can participate in the project, for example:

- Submit bugs and feature requests, and help us verify them
- Submit pull requests for new modules, roles and other content

We're following the general Ansible contributor guidelines;
see [Ansible Community Guide](https://docs.ansible.com/ansible/latest/community/index.html).

If you want to develop new content for this collection or improve what is already here, the easiest way to work on the
collection is to clone this repository (or a fork of it) into one of the configured [`ANSIBLE_COLLECTIONS_PATHS`](
https://docs.ansible.com/ansible/latest/reference_appendices/config.html#collections-paths) and work on it there:
1. Create a directory `ansible_collections/jm1`;
2. In there, checkout this repository (or a fork) as `packages`;
3. Add the directory containing `ansible_collections` to your
   [`ANSIBLE_COLLECTIONS_PATHS`](https://docs.ansible.com/ansible/latest/reference_appendices/config.html#collections-paths).

Helpful tools for developing collections are `ansible`, `ansible-doc`, `ansible-galaxy`, `ansible-lint`, `flake8`,
`make` and `yamllint`.

| OS                                           | Install Instructions                                                |
| -------------------------------------------- | ------------------------------------------------------------------- |
| Debian 10 (Buster)                           | Enable [Backports](https://backports.debian.org/Instructions/). `apt install ansible ansible-doc ansible-lint flake8 make yamllint` |
| Debian 11 (Bullseye)                         | `apt install ansible ansible-lint flake8 make yamllint` |
| Debian 12 (Bookworm)                         | `apt install ansible ansible-lint flake8 make yamllint` |
| Debian 13 (Trixie)                           | `apt install ansible ansible-lint flake8 make yamllint` |
| Fedora                                       | `dnf install ansible python3-flake8 make yamllint` |
| Red Hat Enterprise Linux (RHEL) 7 / CentOS 7 | Enable [EPEL](https://fedoraproject.org/wiki/EPEL). `yum install ansible ansible-lint ansible-doc  python-flake8 make yamllint` |
| Red Hat Enterprise Linux (RHEL) 8 / CentOS 8 | Enable [EPEL](https://fedoraproject.org/wiki/EPEL). `yum install ansible                          python3-flake8 make yamllint` |
| Red Hat Enterprise Linux (RHEL) 9 / CentOS 9 | Enable [EPEL](https://fedoraproject.org/wiki/EPEL). `yum install ansible                          python3-flake8 make yamllint` |
| Ubuntu 18.04 LTS (Bionic Beaver)             | Enable [Launchpad PPA Ansible by Ansible, Inc.](https://launchpad.net/~ansible/+archive/ubuntu/ansible). `apt install ansible ansible-doc ansible-lint flake8 make yamllint` |
| Ubuntu 20.04 LTS (Focal Fossa)               | Enable [Launchpad PPA Ansible by Ansible, Inc.](https://launchpad.net/~ansible/+archive/ubuntu/ansible). `apt install ansible ansible-doc ansible-lint flake8 make yamllint` |
| Ubuntu 22.04 LTS (Jammy Jellyfish)           | `apt install ansible ansible-lint flake8 make yamllint` |
| Ubuntu 24.04 LTS (Noble Numbat)              | `apt install ansible ansible-lint flake8 make yamllint` |

Have a look at the included [`Makefile`](Makefile) for
several frequently used commands, to e.g. build and lint a collection.

## More Information

- [Ansible Collection Overview](https://github.com/ansible-collections/overview)
- [Ansible User Guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)
- [Ansible Developer Guide](https://docs.ansible.com/ansible/latest/dev_guide/index.html)
- [Ansible Community Code of Conduct](https://docs.ansible.com/ansible/latest/community/code_of_conduct.html)

## License

GNU General Public License v3.0 or later

See [LICENSE.md](LICENSE.md) to see the full text.

## Author

Jakob Meng
@jm1 ([github](https://github.com/jm1), [galaxy](https://galaxy.ansible.com/jm1), [web](http://www.jakobmeng.de))

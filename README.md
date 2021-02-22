# Homelab Ansible Roles: GitLab Runners Setup

A set of Ansible roles I use to configure my homelab GitLab runners. Currently written to work only with Debian machines. Installs utilities and QoL admin tools, configures a build environment for my KVM Conjurer project, and registers the runners with my local GitLab controller.

As you can see in the playbook `update-all.yml`, create a folder `secrets/` with vars files containing your GitLab URL, tokens, etc. Configure your inventory how you will. I use an explicit inventory file stored next to my playbook in a folder called `inventory/`.

## Things I'd like to add

* CRUD operations through handlers
* Support for other Linux flavors (Fedora, openSUSE)

## Known issue

* Installing virtinst kicks user out to a grub-pc update. Resolve this programmatically with Ansible

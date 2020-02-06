# Spinnaker-Ansible

Ansible Playbook for installing and configuring Spinnaker

## For Local Development

### Required tools

- Vagrant - `>= 2.2.2`
- Ansible - `>=2.9.2`
- Virtualbox

### Adding Vagrant box to Local environment

```bash
vagrant box add ubuntu/bionic64
```

Verify Vagrant box is updated

```bash
 vagrant box list
generic/rhel7   (virtualbox, 1.9.40)
suse13          (virtualbox, 0)
ubuntu/bionic64 (virtualbox, 20191218.0.0)
ubuntu/xenial64 (virtualbox, 20191105.0.0)
ubuntu/xenial64 (virtualbox, 20191204.0.0)
ubuntu/xenial64 (virtualbox, 20191211.0.0)
```

Start your VM

```bash
vagrant init
```

You can tune your VM configs by updating `Vagrantfile`.

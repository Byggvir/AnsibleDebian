# AnsibleDebian
Install a **Debian** system with **Ansible**

# Prerequisites

We need a minimal **Debian** system with **System Tools** and **sshd**  installed. All other packages will be installed via Ansible.

## Test setup

For testing I used a **Virtual Machine** with the IP address 192.168.2.70. On my DNS server I configured the zone *example.com* with just one entry *minisys*.

When the installed **mini system** (minisys) is up and running, we copy our *public ssh key* to the system.

```
    ssh-copy-id -i .ssh/my_rsa.pub thomas@minisys.example.com
```

We add the private ssh-key to the ssh-agent *(ssh add .ssh/my_rsa )* and cao log into our server with:

```
ssh thomas@minisys.example.com
```

This adds also the host-keys to your known hosts. If you leave this step, the next ansible script will fail.

<u>Remark:</u> There is no need to do this simple step with Ansible.

## Making the mini system Ansible compatible

The *minisys* lacks some packages to fully support Ansible.

The playbook/pb_setup.yaml installs the missing packages for us. It calls the role *minimalsystem*.

Because the user *thomas* is not in the group *sudo* at this time, we must provide a password to become *root*.

```
    ansible-playbook -k playbook/pb_setup.yaml
```

# Enhancing the server

## Linux, Apache, MySQL and PHP Server

To install an Apache *web server* we use the playbook *p b_lamp.yaml*.

```
    ansible-playbook playbook/pb_setup.yaml
```

<u>Remark:</u> With a password-less ssh-key we don't have to provide passwords.


sou-lab-cni
===========

This project allows to create a small environment with vagrant with two virtual machine, the frontend and the backend, the configuration is handled with Ansible, and it uses podman to install basic version of haproxy on the frontend and grafana and prometheus on the backend.

usage
===========

To setup the environment you must run the following commands

```bash
# To setup the virtual machines
vagrant up --no-provision

# To configure the virtual machines with Ansible
vagrant provision
```

explanation
===========

I choose to use the two commands separatley because I want that the playbook is exectued once and for both the vms a the same time,
this behaviour allows to setup some usefull configurations, such as the ip address of the other vm in `/etc/hosts` and the ip address of the backend in the `haproxy.cfg` file.

In the branch `feat/single-command` the solution with the only `vagrant up` command can be found
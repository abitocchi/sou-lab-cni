sou-lab-cni
===========

This project allows to create a small environment with vagrant and two virtual machine, the frontend and the backend, the configuration is handled with Ansible, and it uses podman to install basic version of haproxy on the frontend and grafana and prometheus on the backend.

usage
===========

To setup the environment you must run the following commands

```bash
# To setup the virtual machines
vagrant up

# To configure the virtual machines with Ansible in case they are already deployed
vagrant provision
```

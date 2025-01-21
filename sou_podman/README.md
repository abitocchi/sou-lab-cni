sou_podman
=========

The role allows to configure grafana and prometheus behind haproxy with two virtual machine, haproxy is installed in the frontend and grafana and prometheus in the backend, the role uses podman to install and manage the products


Role Variables
--------------

prometheus_id
grafana_id


Dependencies
------------

- containers.podman

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- name: Provisioner
  hosts: all
  become: true
  roles:
   - sou_podman

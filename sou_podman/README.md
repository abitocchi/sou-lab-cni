sou_podman
=========

The role allows to configure grafana and prometheus behind haproxy with two virtual machine, haproxy is installed in the frontend and grafana and prometheus in the backend, the role uses podman to install and manage the products


Role Variables
--------------
```yaml
prometheus:
  user_id: ""
  host: ""

  scrape_interval: ""
  evaluation_interval: ""

grafana:
  user_id: ""
  host: ""

  config:
    app_mode: ""
    http_port: ""

haproxy:
  user_id: ""

  ssl:
    private_key_path: ""
    certificate_path: ""

  bind:
    address: ""
    extra_params: ""
```


Dependencies
------------

- containers.podman
- community.crypto

Example Playbook
----------------

```yaml
---
- name: Provisioner
  hosts: all
  become: true
  roles:
   - sou_podman
```

Ansible Nginx playbook
=====

This role installs and configures Nginx on a server. It is also able to configure basic virtualhosts.

Requirements
------------

This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

Examples
========

```
- name: nginx server
  hosts: web
  user: root
  roles:
    - role: nginx
      nginx_sites:
        - server:
           file_name: nginx.deimos.lan
           server_name: nginx.deimos.lan
           listen: 80
           root: /usr/share/nginx/www/blog
           location1: {name: /, try_files: "$uri $uri/ /index.html"}
```

Dependencies
------------

None

License
-------

GPL

Author Information
------------------

Pierre Mavro / deimosfr



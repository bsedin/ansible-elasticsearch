# Elasticsearch role for ansible

Create `./library` directory in your ansible project:

```
mkdir ./library
```

And configure `ansible.cfg`:

```
[defaults]
roles_path = ./library
```

Add submodule:

```
git submodule add git@github.com:kressh/ansible-elasticsearch.git library/elasticsearch
```

Use role:

```yaml
---
- hosts: elasticsearch
  remote_user: ansible
  become: true
  roles:
    - elasticsearch
```

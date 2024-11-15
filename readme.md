# asbl-docker_install

## Description

This repo contain the ansible role that configure docker and docker-compose for the servers.
- install docker (rootless or rootfull) and docker compose (docker compose version 1 or 2).
- install docker pip package to be compatible with ansible's docker module.
- Manage user and group related to docker.
- Configure docker daemon.

## Prerequisite

- None

## Usage

### Use role

- Add the role git source in "requirements.yml" file :
```
  - name: role_name
    scm: git
    src: git@github.com:tiny-company/<repository_name>.git
    version: main
```

- And then use the galaxy command to load the file dependencies :
```
ansible-galaxy install -r requirements.yml
```

- Or manually get the playbook as collection (with ansible-galaxy) :
```
ansible-galaxy collection install git@github.com:tiny-company/<repository_name>.git
```

### Variables

For an exhaustive list of variables check the [defaults](defaults/main.yml)
file. Ideally, all values will have commentaries describing what are their
purposes and by the default value you can tell the type.


## Source :

- [nickjj docker role](https://github.com/nickjj/ansible-docker/tree/master)
- [mullholand docker role](https://github.com/mullholland/ansible-role-docker)
- [ansible docker_login module](https://docs.ansible.com/ansible/latest/collections/community/docker/docker_login_module.html)
- [docker rootless install guide](https://docs.docker.com/engine/security/rootless/)
- [docker classic install guide](https://docs.docker.com/engine/install/debian/)

Docker Services
=========

This role will provision a docker container as a service on the target machine.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

```
docker_services: []
```

Service definition should be an object of following specification:

```
name: <string>
description: <string>
run_args: <string> # Optional
image: <string>
environment: <dict<string, string>> # Optional
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: servers
  roles:
      - docker-services
  vars:
    docker_services:
      - name: hello-world
        description: Hello world service to test docker deployment
        run_args: -p "8000:80"
        image: tutum/hello-world
        environment:
          MY_SECRET: secretValue
```

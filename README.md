# Containerized Undercloud Validation Role Progress

Tool to validate containerized undercloud after upgrade from non-containerized,
indeed at any state.  Can be adapted for in-flight testing during uprade etc.

## Implemented

* Container presence, iterating through containers against provided list

## To be implemented

* Ports per container against provided list
* API calls to given services

## Questions

* What version was undercloud pre-containerized?

## Useful Links

* [ansible docker_container](http://docs.ansible.com/ansible/latest/modules/docker_container_module.html#docker-container-module)
* [docker filtering](https://docs.docker.com/engine/reference/commandline/ps/#filtering)
* [docker formatting](https://docs.docker.com/config/formatting/)
* [ansible callback](https://docs.ansible.com/ansible/2.5/plugins/callback.html)
* [ansible stderr](https://docs.ansible.com/ansible/2.5/plugins/callback/stderr.html)

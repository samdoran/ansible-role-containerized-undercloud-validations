# Containerized Undercloud Validation Role Progress

Tool to validate containerized undercloud after upgrade from non-containerized,
indeed at any state.  Can be adapted for in-flight testing during uprade etc.

## Implemented

* Container presence, iterating through containers against provided list

## To be implemented

* Ports per container against provided list
* API calls to given services

## Ports found on containerized undercloud dev env
```bash
(undercloud) [stack@undercloud ~]$ sudo nmap -n -PN -sT -sU -p- 192.168.24.1

Starting Nmap 6.40 ( http://nmap.org ) at 2018-05-30 19:42 UTC
Nmap scan report for 192.168.24.1
Host is up (0.00047s latency).
Not shown: 131031 closed ports
PORT      STATE         SERVICE
22/tcp    open          ssh
111/tcp   open          rpcbind
873/tcp   open          rsync
3000/tcp  open          ppp
3306/tcp  open          mysql
4369/tcp  open          epmd
5000/tcp  open          upnp
5050/tcp  open          mmcc
5672/tcp  open          amqp
6000/tcp  open          X11
6001/tcp  open          X11:1
6002/tcp  open          X11:2
6379/tcp  open          unknown
6385/tcp  open          unknown
8000/tcp  open          http-alt
8004/tcp  open          unknown
8080/tcp  open          http-proxy
8088/tcp  open          radan-http
8774/tcp  open          unknown
8775/tcp  open          unknown
8778/tcp  open          unknown
8787/tcp  open          unknown
8888/tcp  open          sun-answerbook
8989/tcp  open          unknown
9000/tcp  open          cslistener
9292/tcp  open          unknown
9696/tcp  open          unknown
11211/tcp open          unknown
15672/tcp open          unknown
25672/tcp open          unknown
35357/tcp open          unknown
39422/tcp open          unknown
68/udp    open|filtered dhcpc
69/udp    open|filtered tftp
111/udp   open          rpcbind
123/udp   open          ntp
867/udp   open|filtered unknown
6230/udp  open|filtered unknown
6231/udp  open|filtered unknown

Nmap done: 1 IP address (1 host up) scanned in 5.38 seconds
```


## Questions

* What version was undercloud pre-containerized?
* Are keepalived and haproxy supports to be running?

## Useful Links

* [ansible docker_container](http://docs.ansible.com/ansible/latest/modules/docker_container_module.html#docker-container-module)
* [docker filtering](https://docs.docker.com/engine/reference/commandline/ps/#filtering)
* [docker formatting](https://docs.docker.com/config/formatting/)
* [ansible callback](https://docs.ansible.com/ansible/2.5/plugins/callback.html)
* [ansible stderr](https://docs.ansible.com/ansible/2.5/plugins/callback/stderr.html)

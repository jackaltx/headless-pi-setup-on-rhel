# headless-pi-setup-on-centos8
This role will download the RaspiOS imange and tranform it into a headless boot for PiFarm use.

This role executes on the local machine (in my case the farmer).


- create a playbook that will use this role

```
---
- hosts: localhost
  connection: local
  gather_facts: no
  become: yes
  become_method: sudo
  roles:
    - headless-pi-setup
```

Sample executions

- ansible-playbook headless-setup.yml  -K 
- ansible-playbook headless-setup.yml  -K --tags umount
- ansible-playbook headless-setup.yml  -K --tags mount



## Inspired by

1. https://github.com/nihalgonsalves/headless-pi-setup
1. https://github.com/perrygeo/raspberry_pi
1. https://github.com/ssharpjr/rpi-headless-setup
1. https://www.raspberrypi.org/forums/viewtopic.php?t=140538
1. https://github.com/gloveboxes/Raspberry-Pi-Kubernetes-Cluster
1. https://blog.alexellis.io/test-drive-k3s-on-raspberry-pi/   (cgroup)
1. https://github.com/lucasteligioridis/raspbernetes
1. https://github.com/codesqueak/k18srpi4  (disable swap file ??)
1. 

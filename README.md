# Container Security Workstation Playbook

This is a set of playbooks for setting up a container security workstation with common tools for doing container security reviews.

There are three playbooks in the repository

- cli_container_sec_workstation.yml - This has only command line tools installed
- gui_container_sec_workstation.yml - This adds tools that have a GUI but relies on a remote X server being available
- desktop_container_sec_workstation.yml - This installs XFCE4 and xrdp so you can get a remote full desktop.

Rough draft at the moment, still quite a bit of work to do.

## Pre-requisites

- Tested on Ubuntu, may work on other deb based distros
- [Ansible install](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
  - For Ubuntu there's an install script (install_ansible_ubuntu.sh)
- Change the `user` var in the playbook to your username

## Installation Process

Once you've got the pre-requisites installed, you can just run

```
ansible-playbook [playbook-YAML-file]
```
and it should setup the machine as needed.

## Tools List - Core

- [Auger](https://github.com/jpbetz/auger)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [etcdctl](https://etcd.io/)
- [gvisor](https://gvisor.dev/)
- [helm](https://helm.sh/)
- [kind](https://kind.sigs.k8s.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [kubens & kubectx](https://github.com/ahmetb/kubectx)
- [kube-ps1](https://github.com/jonmosco/kube-ps1)
- [nmap](https://nmap.org/)
- [rakkess](https://github.com/corneliusweig/rakkess)
- [kubectl-who-can](https://github.com/aquasecurity/kubectl-who-can)
- [rback](https://github.com/team-soteria/rback)
- [trivy](https://github.com/aquasecurity/trivy/)
- [whaler](https://github.com/P3GLEG/Whaler)
- [dive](https://github.com/wagoodman/dive)
- [kube-bench](https://github.com/aquasecurity/kube-bench/)

## Tools List - GUI

If you install the GUI playbook then it will add some handy tools which require a GUI.  You can then access the VM from a machine with an X Server (e.g. MobaXterm or XMing on Windows) and access these additional tools

- [firefox](https://www.mozilla.org/en-GB/firefox/new/?redirect_source=firefox-com)
- [octant](https://github.com/vmware-tanzu/octant)
- [Visual Studio Code](https://code.visualstudio.com/) , with the Docker, Kubernetes and YAML plugins

## TODO

- Add More tools

# K8S setup with vagrant, ansible, kubeadm

# mini HOWTO

Scripts to install a kubernetes cluster in Vagrant

You need a `bash` enviroment with SSH, either a Linux Distro, a Mac OSX or Windows 10 Bash (see below for Windows)

You need also VirtualBox, Vagrant and Ansible installed in your environment. 

# Setup on Linux/OSX

The kit is for Unix, so works out of the box in Linux and OSX, as follows.

## Create VMs in Virtualbox with vagrant

- `cd servers/vbox`
- `vagrant up`
- `vagrant ssh-config >>~/.ssh/config`

## Edit your `hosts` file

Run `sudo vi /etc/hosts` and add the following line:

`127.0.0.1 master node1 node2 node3`

## Provision Kubernetes with ansible

- `pip install ansible`
- `cd ../../kubernetes`
- `ansible-playbook site.yml`

That is. Once done, `vagrant ssh master` and start playing with `Kubernetes`

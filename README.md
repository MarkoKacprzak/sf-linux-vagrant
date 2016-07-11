# Vagrant setup for Service Fabric on Linux

This repo contains a Vagrant definition for setting up a Ubuntu 15.10-based onebox for Service Fabric.

## Prerequisites

* [Vagrant (v1.8.4 or later)](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Instructions

1. Clone this repo to your development machine.
2. Run 'vagrant up' to create the VM and launch the local cluster.
3. Run 'vagrant ssh' to connect to the VM.

By default, the Vagrantfile creates a private network at 192.168.50.50. You can connect to Service Fabric Explorer at http://192.168.50.50:19080/Explorer.

## Joining the Service Fabric Linux preview program

If you happened upon this repo and are interested in officially joining the Service Fabric Linux preview, please follow the instructions [here](http://aka.ms/sflinux).

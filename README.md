# packer-arch-chef

This [Packer](https://packer.io/) template will create a [Vagrant](https://www.vagrantup.com/) box running [Arch Linux](http://archlinux.org/) with [Chef](http://chef.io/) preinstalled, using the [Virtualbox](https://virtualbox.org) provider.

It is derived from the [packer-arch](https://github.com/elasticdog/packer-arch) template by [@elasticdog](https://github.com/elasticdog).

If you need something similar for Docker containers, take a look at [docker-archlinux-chef](https://github.com/logankoester/docker-archlinux-chef).

## Usage

Assuming that you already have Packer,
[VirtualBox](https://www.virtualbox.org/), and Vagrant installed, you
should be good to clone this repo and go:

    $ git clone https://github.com/logankoester/packer-arch-chef.git
    $ cd packer-arch-chef/
    $ packer build arch-chef-template.json

Then you can import the generated box into Vagrant:

    $ vagrant box add arch packer_arch_chef_virtualbox.box

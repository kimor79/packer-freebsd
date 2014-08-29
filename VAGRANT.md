Vagrant Specific
================

The following have been added to the image (in addition to those listed in [README.md](README.md)):

  * For VirtualBox: See [VIRTUALBOX.md](VIRTUALBOX.md)
  * Root password is set to *vagrant*
  * The user *vagrant* has been added with password *vagrant* and authorized_keys from https://github.com/mitchellh/vagrant/raw/master/keys/vagrant.pub

To build a VirtualBox Vagrant box:

  1. `rm -f /tmp/packer-freebsd-10.0-amd64-patches-vagrant-vbox-*`
  1. `packer build --only=vbox4vagrant freebsd-10.0-amd64-patches.json`
  1. `vagrant box add --force packer-freebsd-10.0-amd64-patches-vagrant-vbox /tmp/packer-freebsd-10.0-amd64-patches-vagrant-vbox-*.box`
  1. `vagrant up`
  1. Smoke test (e.g., `vagrant ssh` and look around)

Vagrant boxes:

  * None as of 2014-08-29

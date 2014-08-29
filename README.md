Building a FreeBSD image
========================

This repo contains packer templates and related files to build a FreeBSD image.

Available templates:

  * [FreeBSD 10.0 amd64 with security patches](freebsd-10.0-amd64-patches.json)

The following sets are installed:
  * base
  * kernel
  * lib32
  * ports
  * src

Here are the additions to the base install:

  * The timezone is set to UTC
  * pkgng is installed
  * ntpd and ntpdate are enabled
  * sshd is enabled
  * *UseDNS* is set to *no* in /etc/ssh/sshd_config

Available builders:

  * [vbox4vbox](VIRTUALBOX.md) - build a box for VirtualBox

Vagrant boxes:

  * None as of 2014-08-29

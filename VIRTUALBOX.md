VirtualBox Specific
===================

The following have been added to the image (in addition to those listed in [README.md](README.md)):

  * The virtualbox-ose-additions package is installed
  * Root password is set to *root*

To build a VirtualBox box:

  1. `rm -f /tmp/packer-freebsd-10.0-amd64-patches-vbox-*`
  1. `packer build --only=vbox4vbox freebsd-10.0-amd64-patches.json`
  1. Launch `/tmp/packer-freebsd-10.0-amd64-patches-vbox-*/*.vmdk` in VirtualBox
  1. Smoke test (e.g., login via console and look around)

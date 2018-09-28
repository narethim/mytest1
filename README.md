# mytest1
Experimental

### Overview

This repository contains [Packer](https://packer.io/) templates for creating Ubuntu Vagrant boxes.

## Current Boxes

We no longer provide pre-built binaries for these templates.

## Building the Vagrant boxes with Packer

To build all the boxes, you will need [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

We make use of JSON files containing user variables to build specific versions of Ubuntu.
You tell `packer` to use a specific user variable file via the `-var-file=` command line
option.  This will override the default options on the core `ubuntu.json` packer template,
which builds Ubuntu 16.04 by default.

For example, to build Ubuntu 16.04, use the following:

    $ packer build -var-file=ubuntu1604.json ubuntu.json
    
If you want to make boxes for a specific desktop virtualization platform, use the `-only`
parameter.  For example, to build Ubuntu 16.04 for VirtualBox:

    $ packer build -only=virtualbox-iso -var-file=ubuntu1604.json ubuntu.json

The boxcutter templates currently support the following desktop virtualization strings:

* `virtualbox-iso` - [VirtualBox](https://www.virtualbox.org/wiki/Downloads) desktop virtualization

## Building the Vagrant boxes with Packer (Again)

To build all the boxes, you will need [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

    $ packer validate ubuntu.json

Some text

    * `abc.txt` - Some abc.text file
    * `abc2.txt` - Some abc2.text file
    

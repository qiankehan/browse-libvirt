# How to build libvirt

## Install dependencies
Make *source repository* is configurated.  

### For Fedora/Centos
Install dependencies via *dnf builddep*:
```sh
dnf builddep libvirt -y
```
For earlier fedora/centos, install *yum-utils* first and then install 
dependencies via *yum-builddep*:
```sh
yum install yum-utils -y && yum-builddep libvirt -y
```

### For Debian/Ubuntu
Install dependencies by *apt build-dep*:
```sh
apt build-dep libvirt0 -y
```

## Download the code
According to [libvirt download page](https://libvirt.org/downloads.html), 
download your preferred libvirt version at https://libvirt.org/sources/ . Or 
download libvirt source via git:
```sh
git clone git://libvirt.org/libvirt.git
```

## Configuration
Libvirt is built by 
[GNU build system](https://en.wikipedia.org/wiki/GNU_Build_System).
1. Change to libvirt source directory.
1. Generate automake/autoconf scripts: `./autogen.sh`
1. Run `configure` script to finish configuration before compilation: 
`./configure`  
To use customized configuration options, run `./configure --help` to get all 
the configuration options and influential environment variables.

## Make
Build libvirt by [make](https://en.wikipedia.org/wiki/Make_%28software%29). Run 
*make* command by your purpose:
- build libvirt project: `make`
- build libvirt doc html only: `make html`
- check the code syntax only: `make syntax-check`
- build libvirt and run unit tests: `make check`

## Installation
For rpm target files, install and uninstall them by *rpm*. The rpm files are in 
**~/rpmbuild/RPMS/x86_64/**.  
To install target files by make, run `sudo make install` in the code directory. 
To uninstall them, run `sudo make uninstall`.

## Build by build system of distributions
Different linux distributions integrate the above processes into their build 
script and build libvirt by their build system. The following is the build script 
and build system of major linux distributions.
- rhel/centos/fedora: build processes defined by 
[spec file](http://ftp.rpm.org/max-rpm/s1-rpm-inside-scripts.html) and built by 
[rpmbuild](https://linux.die.net/man/8/rpmbuild)
- debian/ubuntu: build processes defined by 
[control and rules file](https://www.debian.org/doc/manuals/maint-guide/dreq.en.html), 
built by [debuild](https://wiki.debian.org/BuildingTutorial)
- arch linux: build processes defined by 
[PKGBUILD file](https://wiki.archlinux.org/index.php/PKGBUILD) and built by 
[asp](https://github.com/archlinux/asp)
- gentoo linux: build processes defined by 
[ebuild file](https://wiki.gentoo.org/wiki/Basic_guide_to_write_Gentoo_Ebuilds) 
and built by
[ebuild](https://dev.gentoo.org/~zmedico/portage/doc/man/ebuild.1.html)

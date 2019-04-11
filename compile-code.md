# Compile Libvirt
## Install dependencies
### For Fedora/Centos
Make *source repository* is configurated.  
Install dependencies via *dnf builddep*:
```sh
dnf builddep libvirt -y
```
For earlier fedora/centos, install *yum-utils* first and then install dependencies 
via *yum-builddep*:
```sh
yum install yum-utils -y && yum-builddep libvirt -y
```

### For Debian/Ubuntu
Make *source repository* is configurated, too.  
Install dependencies by *apt build-dep*:
```sh
apt build-dep libvirt0 -y
```

## Download the code

## Configuration

## Make

## Installation


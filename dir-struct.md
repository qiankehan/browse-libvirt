# Directory Structure
Check libvirt code directory after download. There are following sub-directory 
in libvirt root directory:
- **build-aux**: The [autoconf](https://www.gnu.org/software/autoconf/) auxiliary directory.
- **docs**: Include the documents of libvirt and libvirt [relax-ng](https://relaxng.org/) 
schema. The former could be seen on [libvirt org site](https://libvirt.org/).
The later is used for libvirt xml validation, such as [virt-xml-validate](https://linux.die.net/man/1/virt-xml-validate).
- **example**: This directory contains libvirt API usage examples.
- **gnulib**: [The GNU Portability Library](https://www.gnu.org/software/gnulib/). 
A library that libvirt relies on.
- **include**: Libvirt public header files.
- **m4**: [GNU M4](https://www.gnu.org/software/m4/), a Unix macro processor, is a 
dependency of GNU autoconf.
- **po**: [GetText](https://en.wikipedia.org/wiki/Gettext) related files, they are 
used for [internationalization and localization](https://en.wikipedia.org/wiki/Internationalization_and_localization).
- **src**: The libvirt core library codes.
- **tests**: Libvirt unit test files.
- **tools**: The codes libvirt supplementary programs, such as [virsh](https://linux.die.net/man/1/virsh), 
virsh shell completion, 
[libvirt-guests service](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/virtualization_administration_guide/sub-sect-shutting_down_rebooting_and_force_shutdown_of_a_guest_virtual_machine-manipulating_the_libvirt_guests_configuration_settings), 
[libvirt wireshark dissector](https://github.com/libvirt/libvirt/tree/master/tools/wireshark), 
[libvirt-nss](https://wiki.libvirt.org/page/NSS_module), 
[virt-admin](https://www.systutorials.com/docs/linux/man/1-virt-admin/), 
[virt-login-shell](https://manpages.ubuntu.com/manpages/trusty/man1/virt-login-shell.1.html), 
[virt-host-validate](https://linux.die.net/man/1/virt-host-validate), 
[virt-pki-validate](https://linux.die.net/man/1/virt-pki-validate), 
[virt-xml-validate](https://linux.die.net/man/1/virt-xml-validate), 
[virt-sanlock-cleanup](https://linux.die.net/man/8/virt-sanlock-cleanup).

## schema
Libvirt use xml to record or manage resources, including **domain**, 
**domain snapshot**, **nodedev**, **secret**, **storagevol**, **capability**, 
**interface**, **nwfilter**, **nwfilterbinding**, **network**.  
The relax-ng schema files define the format of libvirt xml


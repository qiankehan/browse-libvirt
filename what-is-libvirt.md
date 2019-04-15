# What is libvirt
[Libvirt](https://libvirt.org/) is a toolkit to manage virtualization platforms.

## What libvirt can do
- Manage virtualization hypervisors: 
[QEMU/KVM](https://libvirt.org/drvqemu.html), 
[Xen](https://libvirt.org/drvxen.html), 
[Virtuozzo](https://libvirt.org/drvvirtuozzo.html), 
[OpenVZ](https://libvirt.org/drvopenvz.html), 
[VMWare ESX](https://libvirt.org/drvesx.html), 
[VMware Workstation/Player/Fusion](https://libvirt.org/drvvmware.html), 
[VirtualBox](https://libvirt.org/drvvbox.html), 
[LXC](https://libvirt.org/drvlxc.html), 
[BHyve](https://libvirt.org/drvbhyve.html), 
[IBM PowerVM](https://libvirt.org/drvphyp.html), 
[Microsoft Hyper-V](https://libvirt.org/drvhyperv.html)
- Manage host resources: 
[storages](https://libvirt.org/storage.html), 
[networks](https://libvirt.org/formatnetwork.html), 
[host node devices](https://libvirt.org/drvnodedev.html), 
[network filters](https://libvirt.org/formatnwfilter.html), 
[host interfaces](https://libvirt.org/devhelp/libvirt-libvirt-interface.html)

## Preparation to review the code
### Download the code
Use **git** to download [libvirt source code](https://libvirt.org/downloads.html#git).  
```sh
git clone git://libvirt.org/libvirt.git
```

### Learn git
Git is powerful version-control system for tracking changes in source code. 
The following git sub-commands are useful for browsing the code.
### git log
Git log is to show the commits history of the source code.  
Run it directly in the source code directory then get the commits from the last to the first:
```sh
git log
```
By format strings, you can set the format of commits log. [This link](https://devhints.io/git-log-format) 
gives the full format or git log.
For example, see the *commit hash*, *author*, *author date*, *commit subject*:
```sh
git log --pretty="format:%H %an %aD %s"
```

And it can get the commits from one to another:
```sh
git log COMMIT1..COMMIT2
```
By using tags, you can find the commits during two versions. For example, the 
following command will show the commits between version v4.5.0 to v4.6.0 :
```sh
git log v4.5.0..v4.6.0
```
  
Man page: [git log](https://git-scm.com/docs/git-log)

### git tag
**Tags** are ref's that point to specific points in **Git** history.  Tagging is generally 
used to capture a point in history that is used for a **marked version release** (i.e. v1.0.1).  
Run as following in source code dir to show all the tags:
```sh
git tag
```
**--contains** is to show which tags contains a specific commit:
```sh
git tag --contains COMMIT
```
  
Man page: [git tag](https://git-scm.com/docs/git-tag)

### git show
**Git show** can check the detailed changes of commits.  
To show the latest code change of a commit:
```sh
git show
```
Show code change of specific commit:

  
Man page: [git show](https://git-scm.com/docs/git-show)


## vim plugins
### fugitive.vim
[fugitive.vim](https://github.com/tpope/vim-fugitive) is a nice git wrapper of vim.   
You can use [pathogen.vim](https://github.com/tpope/vim-pathogen) or [Vundle.vim
](https://github.com/VundleVim/Vundle.vim) to install it.  
See chapter Practice, *how to use vim&git to find which software versions contain 
the code of a specific line*.


{% dot %}
graph graphname {
  a -- b -- c;
  b -- d;
}
{% enddot %}

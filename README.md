This repository contains the [FAI](fai) configuration directory, mainly used
for bootstrapping LXC containers to our local machine.

Before running FAI create the container and configure it (edit
`/var/lib/lxc/my_host/config`).

    # lxc-create -n my_host

As we are bootstrapping on our local machine we can run FAI without PXE; this
saves us from configuring DHCP and TFTP.

    # fai -N -v -u my_host -s file:///srv/fai/config \
        dirinstall /var/lib/lxc/my_host/rootfs/

-----
Jordi Funollet <jordi.f@ati.es>    
Tue, 24 Jan 2012 17:10:35 +0100



[fai]: http://fai-project.org/

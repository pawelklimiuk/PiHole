# PiHole
from.... https://discourse.pi-hole.net/t/dynamic-update-of-dns-with-dhcp-lease-info-between-dual-redundant-pihole-servers/65027/3
PiHole add on ;)

The two files listed above (SyncDHCP.sh,SyncDHCP.service) are all it takes.

Configuration:

    Copy the files to the given directory and set permissions (.sh must be chmod'd 744)
    Establish public key authentication between root on both systems
        apt install openssh-server
        ssh-keygen ...
        ssh-copy-id ...
    Install inotify-tools (apt install inotify-tools)
    Enable the service (systemctl enable SyncDHCP.service)

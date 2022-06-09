# Debian Bootstrap

The following README.md is the documentation relating to managing and bootstraping debian hosts.

This playbook requires /root/.ssh/authorized_keys & direct root login to host.
When bootstraping a Raspberry Pi copy "docs/rpi-sysconf.txt" to the SD card.

Example files and my general notes are located in the "docs" directory.

Note: I limit system access via the following methods:
 * disabled root password.
 * /ets/hosts.allow (default deny)
 * ufw hostbased firewall.

## Ansible Playbook

| File/Dir Name | Description |
| :--- | :--- |
| ** main.yaml ** | Debian bootstrap / management |
| backup.yaml     | Create a backup of a server |

### Ansible Tasklists

| File/Dir Name | Description |
| :--- | :--- |
| debian_bastion.yaml    | GeoIP config for Bastion hosts |
| debian_cleanup.yaml    | Perform cleanup |
| debian_interfaces.yaml | Configure debian interfaces |
| debian_router.yaml     | Configure host as network router |
| debian_syncthing.yaml  | Install syncthing on host |
| debian_ufw.yaml        | Configure local firewall |

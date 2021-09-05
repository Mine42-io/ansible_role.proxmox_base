# Ansible role - `proxmox_base`

Setup a ProxmoxVE server:

| Tasks file       | Description                                     |
|------------------|-------------------------------------------------|
| `repository.yml` | Enable or disable PVE entreprise APT repository |
| `firewall.yml`   | Configure PVE cluster-wide firewall             |

## Tags

| Tags       | Description                            |
|------------|----------------------------------------|
| `setup`    | Setup ProxmoxVE server                 |
| `teardown` | Remove managed ProxmoxVE configuration |
| `remove`   | Remove managed ProxmoxVE configuration |

## Variables

See `defaults/main.yml` for the full list of variables.

| Variable                | Type   | Required | Defaut | Description                                     |
|-------------------------|--------|----------|--------|-------------------------------------------------|
| `proxmox_base_licensed` | `bool` | No       | `no`   | True if the server is licensed, False otherwise |
| `proxmox_base_fw_rules` | `list` | No       | -      | Firewall rules. Default rules only allow SSH    |

## Templates

| Template                     | Description                         |
|------------------------------|-------------------------------------|
| `pve_firewall_cluster.fw.j2` | Cluster-wide firewall configuration |

## External resources

* https://pve.proxmox.com/wiki/User_Management
* https://pve.proxmox.com/wiki/Firewall

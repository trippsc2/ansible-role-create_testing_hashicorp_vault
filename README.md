<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: trippsc2.create_testing_hashicorp_vault
This role configures Hashicorp Vault in development mode for use in Molecule testing.

## Requirements

| Platform | Versions |
| -------- | -------- |
| Debian | bullseye, bookworm |
| EL | 8, 9 |
| Ubuntu | focal, jammy, noble |

## Dependencies

| Collection |
| ---------- |
| microsoft.ad |

## Role Arguments
|Option|Description|Type|Required|Choices|Default|
|---|---|---|---|---|---|
| vault_token | The token to use for authenticating to Vault. | str | yes |  |  |
| vault_listen_address | The address on which Vault will listen. | str | no |  | {{ vault_ip_address }} |
| vault_listen_port | The port on which Vault will listen. | int | no |  | 8200 |
| vault_configure_firewalld | Whether to configure firewalld. If Debian-based, this will default to false. If Red Hat-based, this will default to true. | bool | no |  | true |
| vault_configure_ufw | Whether to configure ufw. If Debian-based, this will default to true. If Red Hat-based, this will default to false. | bool | no |  | true |
| vault_ip_address | The IP address of the host on which Vault is running. | str | no |  | {{ ansible_host }} |


## License
MIT

## Author and Project Information
Jim Tarpley
<!-- END_ANSIBLE_DOCS -->

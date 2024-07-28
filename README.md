# Ansible role: sops
Mozilla SOPS: management of kubernetes secrets

+ Create Age identity for use with SOPS: `age-keygen -o ~/.config/sops/age/keys.txt`
+ For use with flux, copy private key to a [secret](https://fluxcd.io/flux/guides/mozilla-sops/#encrypting-secrets-using-age)

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `sops_version` (default: latest Github release): which version to install.
+ `sops_encrypter` (default: age): package to install to provide encryption: age, gpg, etc.

## Playbooks
+ `main.yml`: apply role
+ `uninstall.yml`: remove. Run prior to removing host from inventory group.

## Dependencies
None

## License
+ Ansible role licensed [MIT](LICENSE)
+ SOPS licensed MPL 2.0

## Author Information
+ Ansible role by [Sean Ho](https://github.com/ho-ansible/)
+ [SOPS](https://getsops.io/)

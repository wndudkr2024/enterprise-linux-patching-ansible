# Enterprise Linux Patch Automation with Ansible

A production-style Ansible portfolio project for automating RHEL / Oracle Linux patching across multiple environments.

## What this project demonstrates

- Ansible role-based automation
- RHEL / Oracle Linux patch workflows
- Environment-specific inventories
- `group_vars` / `host_vars`
- Reboot handling
- Patch pre-checks and post-checks
- Idempotent playbook design
- Enterprise-style documentation

## Repository structure

```text
inventories/
  dev/
  prod/
roles/
  patching/
playbooks/
docs/
```

## Example usage

```bash
ansible-playbook -i inventories/dev/hosts.ini playbooks/site.yml
```

Run in check mode:

```bash
ansible-playbook -i inventories/dev/hosts.ini playbooks/site.yml --check
```

## Intended use case

This project is designed for enterprise Linux teams that need a repeatable and auditable patching workflow for RHEL-compatible servers.

## Disclaimer

This is a sanitized portfolio project. It does not contain proprietary company code or production customer data.

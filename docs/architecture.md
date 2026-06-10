# Architecture

This project uses a standard Ansible role layout to separate patching logic from inventory-specific configuration.

## Components

- `inventories/dev`: non-production test inventory
- `inventories/prod`: production-style inventory
- `roles/patching`: reusable patch automation role
- `playbooks/site.yml`: main orchestration entry point

## Design principles

- Keep automation idempotent
- Separate environment data from role logic
- Support dry-run validation with `--check`
- Log pre-check and post-check results

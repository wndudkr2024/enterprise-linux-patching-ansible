# Enterprise Linux Patch Automation with Ansible

Production-style Ansible framework for patching RHEL-compatible Linux servers using role-based architecture and Infrastructure as Code practices.

---

## Overview

This project demonstrates a reusable and maintainable Ansible automation framework for enterprise Linux patch management.

The framework is designed to support multiple environments and follows Infrastructure as Code principles to ensure consistency, scalability, and operational reliability.

---

## Features

* Role-based Ansible automation
* Hierarchical inventories
* Environment-specific configurations
* group_vars and host_vars support
* Security-only patch mode
* Full patch mode
* Package exclusion support
* Automatic reboot handling
* Pre-check and post-check validation
* Idempotent execution
* Patch execution logging

---

## Architecture

```text
site.yml
    ↓
patching role
    ↓
precheck.yml
    ↓
patch.yml
    ↓
reboot
    ↓
postcheck.yml
```

---

## Project Structure

```text
.
├── inventories
│   ├── dev
│   │   ├── group_vars
│   │   └── host_vars
│   └── prod
│       ├── group_vars
│       └── host_vars
├── playbooks
│   └── site.yml
├── roles
│   └── patching
│       ├── defaults
│       ├── handlers
│       ├── tasks
│       │   ├── precheck.yml
│       │   ├── patch.yml
│       │   └── postcheck.yml
│       ├── templates
│       └── vars
├── docs
└── README.md
```

---

## Technologies

* Ansible
* Red Hat Enterprise Linux (RHEL)
* Oracle Linux
* YAML
* Jinja2
* Infrastructure as Code

---

## Example Usage

Run against the development inventory:

```bash
ansible-playbook \
-i inventories/dev/hosts.ini \
playbooks/site.yml
```

Run in check mode:

```bash
ansible-playbook \
-i inventories/dev/hosts.ini \
playbooks/site.yml \
--check
```

---

## Design Principles

This project was designed with the following goals:

* Maintainability
* Reusability
* Idempotency
* Separation of logic and configuration
* Environment-specific customization
* Production-style role structure

---

## Intended Use Cases

* Enterprise Linux patch automation
* RHEL and Oracle Linux lifecycle management
* Standardized patching workflows
* Infrastructure as Code initiatives
* Repeatable and auditable operations

---

## Future Enhancements

Planned improvements include:

* GitHub Actions CI pipeline
* yamllint
* ansible-lint
* Molecule testing
* Health checks
* Rollback capability
* Email notifications
* Slack notifications

---

## Disclaimer

This repository is a portfolio project created to demonstrate enterprise automation practices.

No proprietary company code, confidential information, or customer data is included.

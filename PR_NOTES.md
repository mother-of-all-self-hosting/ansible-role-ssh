# PR notes

- Added `system_security_ssh_allow_tcp_forwarding` toggle (default `false`) and wired it into `sshd_config` template; goal is to let consumers enable TCP forwarding without duplicating directives via `system_security_ssh_extension`.
- Tidied tasks for lint/best-practice: named blocks, FQCN for modules, quoted modes.
- Updated metadata accuracy: `role_name: ssh`, restored Archlinux platform entry, kept EL at `7` to mirror upstream’s original declaration even though ansible-lint flags schema on that value; if upstream wants broader EL support or schema-compliant minors (e.g., `7.1`/`7.2`), adjust accordingly.
- Raised `min_ansible_version` to `2.12` to reflect reliance on modern ansible-core/FQCN usage; older `2.1` would not realistically work.

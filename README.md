# system/security/ssh

That role manages sshd configuration and authorized/unauthorized ssh keys

> **NOTE**: check [defaults/main.yml](./defaults/main.yml) to see full list of config options

Common options:
- `system_security_ssh_allow_tcp_forwarding` (bool, default `false`): controls `AllowTcpForwarding` in `sshd_config`

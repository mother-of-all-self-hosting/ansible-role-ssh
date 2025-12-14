# system/security/ssh

This role manages sshd configuration and authorized/unauthorized SSH keys.

<<<<<<< HEAD
> **NOTE**: See [`defaults/main.yml`](./defaults/main.yml) for the full list of variables and defaults.  
> Useful references: sshd_config manual (https://man.openbsd.org/sshd_config), Mozilla OpenSSH guidelines (https://infosec.mozilla.org/guidelines/openssh), openSUSE SSH guide (https://doc.opensuse.org/documentation/leap/security/html/book-security/cha-ssh.html#ex-sshd-conf)
=======
> **NOTE**: check [defaults/main.yml](./defaults/main.yml) to see full list of config options
>
> Useful references for option semantics and hardening:
> - sshd_config manual: https://man.openbsd.org/sshd_config
> - Mozilla OpenSSH guidelines: https://infosec.mozilla.org/guidelines/openssh
<<<<<<< HEAD
>>>>>>> e2c4365 (Add external references for sshd options)
=======
> - openSUSE SSH configuration guide: https://doc.opensuse.org/documentation/leap/security/html/book-security/cha-ssh.html#ex-sshd-conf
>>>>>>> 2768b9b (Add openSUSE SSH guide reference)

Common options:
- `system_security_ssh_allow_tcp_forwarding` (bool, default `false`): controls `AllowTcpForwarding`; enable for SSH tunnels/VS Code Remote
- `system_security_ssh_accept_env` (string, default `"LANG LC_*"`): value for `AcceptEnv`
- `system_security_ssh_allow_stream_local_forwarding` (bool, default `false`): controls `AllowStreamLocalForwarding`
- `system_security_ssh_authorized_keys_file` (string, default `".ssh/authorized_keys /var/ssh/%u"`): value for `AuthorizedKeysFile`
- `system_security_ssh_challenge_response_authentication` (bool, default `false`)
- `system_security_ssh_client_alive_interval` (int, default `120`)
- `system_security_ssh_compression` (bool, default `false`)
- `system_security_ssh_gateway_ports` (bool, default `false`)
- `system_security_ssh_ignore_rhosts` (bool, default `true`)
- `system_security_ssh_login_grace_time` (int, default `0`)
- `system_security_ssh_max_auth_tries` (int, default `3`)
- `system_security_ssh_permit_empty_passwords` (bool, default `false`)
- `system_security_ssh_permit_tunnel` (bool, default `false`)
- `system_security_ssh_x11_forwarding` (bool, default `false`)
- `system_security_ssh_print_last_log` (bool, default `true`)
- `system_security_ssh_print_motd` (bool, default `false`)
- `system_security_ssh_pubkey_authentication` (bool, default `true`)
- `system_security_ssh_sftp_server` (string, default `"/usr/lib/openssh/sftp-server"`)
- `system_security_ssh_use_dns` (bool, default `false`)
- `system_security_ssh_use_pam` (bool, default `true`)

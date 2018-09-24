[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

tinc
====

Installs and configures tinc

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                      | Default                                     | Description |
|---------------------------|---------------------------------------------|-------------|
| tinc_netname              | netname                                     |             |
| tinc_startup_networks     | ["{{ tinc_netname }}"]                      |             |
| tinc_bind_to_address      | ''                                          |             |
| tinc_bind_to_address_port | "{{ tinc_host_port }}"                      |             |
| tinc_bind_to_interface    | ''                                          |             |
| tinc_broadcast            | mst                                         |             |
| tinc_connect_to           | []                                          |             |
| tinc_decrement_ttl        | no                                          |             |
| tinc_device               | ''                                          |             |
| tinc_device_type          | ''                                          |             |
| tinc_direct_only          | no                                          |             |
| tinc_forwarding           | internal                                    |             |
| tinc_graph_dump_file      | ''                                          |             |
| tinc_hostnames            | no                                          |             |
| tinc_iff_one_queue        | no                                          |             |
| tinc_interface            | ''                                          |             |
| tinc_key_expire           | 3600                                        |             |
| tinc_local_discovery      | no                                          |             |
| tinc_mac_expire           | 600                                         |             |
| tinc_max_timeout          | 900                                         |             |
| tinc_mode                 | router                                      |             |
| tinc_name                 | "{{ tinc_netname }}"                        |             |
| tinc_ping_interval        | 60                                          |             |
| tinc_ping_timeout         | 5                                           |             |
| tinc_priority_inheritance | no                                          |             |
| tinc_private_key_file     | "/etc/tinc/{{ tinc_netname }}/rsa_key.priv" |             |
| tinc_process_priority     | ''                                          |             |
| tinc_proxy                | ''                                          |             |
| tinc_replay_window        | 16                                          |             |
| tinc_strict_subnets       | no                                          |             |
| tinc_tunnel_server        | no                                          |             |
| tinc_udp_rcv_buf          | ''                                          |             |
| tinc_udp_snd_buf          | ''                                          |             |
| tinc_host_address         | "{{ ansible_hostname }}"                    |             |
| tinc_host_address_port    | "{{ tinc_host_port }}"                      |             |
| tinc_host_cipher          | blowfish                                    |             |
| tinc_host_clamp_mss       | yes                                         |             |
| tinc_host_compression     | 0                                           |             |
| tinc_host_digest          | sha1                                        |             |
| tinc_host_indirect_data   | no                                          |             |
| tinc_host_mac_length      | 4                                           |             |
| tinc_host_pmtu            | 1514                                        |             |
| tinc_host_pmtu_discovery  | yes                                         |             |
| tinc_host_port            | 655                                         |             |
| tinc_host_subnets         | []                                          |             |

Dependencies
------------

None

Example Playbook
----------------

Installs tinc
```
- hosts: servers
  roles:
    - { role: kbrebanov.tinc }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov

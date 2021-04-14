powervs-bastion-as-router
=========================

This module configures the bastion to be used as a router for the private OCP
network. This allows all nodes in the cluster access to public networks.

Requirements
------------

- firewalld service running with firewall-cmd client
- dhcpd service running

Role Variables
--------------

| Variable            | Required | Default | Comments                |
|---------------------|----------|---------|-------------------------|
| router_interface    | no       | env3    | bastion interface name  |
| private_network_mtu | no       | 1450    | MTU option set by dhcpd |

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Configure bastion as public router
    - hosts: bastion
      roles:
        - powervs-bastion-as-router

License
-------

See LICENCE.txt

Author Information
------------------

Jay Carman <jwcarman@us.ibm.com>

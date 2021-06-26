FreeIPA Docker Role
=========

Ansible role for setting up multi-master FreeIPA realm using Docker.

<!-- Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required. -->

Role Variables
--------------

<!-- A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well. -->

Variable                 | Description
------------------------ | ----------------------------------
`fqdn`                   | Host FQDN
`ip_address`             | Main server IP address
`domain_name`            | Domain
`freeipa_role`           | FreeIPA server role: `master` or `replica`
`freeipa_realm`          | FreeIPA realm name
`freeipa_init_dns`       | DNS server before deployment
`freeipa_forwarder`      | FreeIPA DNS Forwarder
`freeipa_ds_password`    | FreeIPA Directory Manager password
`freeipa_admin_password` | FreeIPA admin user password

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Setup FreeIPA Master
      hosts: freeipa_master
      become: yes
      roles:
        - freeipa_docker

    - name: Setup FreeIPA Replicas
      hosts: freeipa_replicas
      become: yes
      roles:
        - freeipa_docker

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Role Name
=========

A RHN registration role. It will not unsubscribe and re-register if the system is already registered.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `rhn_username` | lookup('env','RHN_USERNAME') | Red Hat Portal username. |
| `rhn_password` | lookup('env','RHN_PASSWORD') | Red Hat Portal password. |
| `rhn_unregister` | null | Whether to unregister. |
| `rhn_register_server_url` | undefined | RHN server hostname  |
| `rhn_register_base_url` | undefined | RHN server base URL |
| `rhn_register_force` | true | Whether to force subscriptioin. |
| `rhn_register_auto_attach` | null | Whether to auto-attach. |

A username and password may be also set at system level by exporting the variables RHN_USERNAME and RHN_PASSWORD.

**Deprecated variables**

These variables are deprecated and will be removed.


| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `rhn_unsubscribe` | null | Whether to unregister (same as rhn_unregister). |

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-rhn-register: { rhn_username: mysuser@redhat.com, rhn_password: changeme }


Testing
-------

1. Export a test inventory, otherwise it will run on localhost:

`export TEST_INVENTORY=/home/opiske/code/infra/test-inventory-ansible/hosts`

2. Run:
`make test`

License
-------

Apache 2.0


Author Information
------------------

Messaging QE team @ redhat.com

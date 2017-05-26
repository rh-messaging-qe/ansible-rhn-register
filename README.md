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
| `rhn_unsubscribe` | null | Whether to unsubscribe. |

A username and password may be also set at system level by exporting the variables RHN_USERNAME and RHN_PASSWORD.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - rhn-subscribe: { rhn-subscribe: mysuser@redhat.com, rhn_password: changeme }


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

Role Name
=========

A RHN registration role suitable for internal use.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `rhn_username` | `qa@redhat.com` | Red Hat Portal username. |
| `rhn_password` | `changeme` | Red Hat Portal password. |

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

Author Information
------------------

messaging-qe@redhat.com

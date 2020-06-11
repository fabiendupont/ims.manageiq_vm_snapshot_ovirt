IMS - ManageIQ - Manage oVirt/RHV VM Snapshots
==============================================

This role allows creating, deleting and reverting snapshots for oVirt / RHV
virtual machines. It also handles VM shutdown when the snapshot requires
quiescing the disks.

Requirements
------------

The role is meant to be run via ManageIQ Embedded Ansible, because the
credentials are passed as an extra variable at runtime.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: fdupont_redhat.ims_manageiq_vm_snapshot_ovirt
          role_action: "create"
          snapshot_name: "Before convert2rhel"
          snapshot_mode: "cold"

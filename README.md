Mount
=========

This role manages mounts on the system. By default the role won't make any changes unless the mount variable is defined.


Role Variables
--------------

mount (REQUIRED)

NOTE: The role accepts the same parameters as the Ansible mount module and behaves in the same way.


Example Playbook
----------------

The recommended way of using this role is to include the role in the top play (that runs on all nodes)
and define the variable in group_vars or host_vars files as needed.


Example role include in play:

```
  - hosts: all
    roles:
    - Mount
```


Variable declaration:

```
  mount_host_list:
   - src: "someserver:/share/vol1"
     dest: /mounts/vol1
     fstype: nfs
   - src: "//someserver/Awesome/Share"
     dest: /mounts/Share
     opts: "uid=user1,user=user1,password=123"
     fstype: cifs
```


Help
----

http://docs.ansible.com/mount_module.html


Author Information
------------------

Tal Lannder

Tal@Pjili.com

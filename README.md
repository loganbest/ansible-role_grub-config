grub
=========

This role modifies the GRUB defaults to how you'd like.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

List of variables used by the role:

```
# Default list of additional Grub command line arguments
grub_cmdline_add_args: []
# Example:
#grub_cmdline_add_args:
#  - biosdevname=0
#  - net.ifnames=0

# Default list of arguments to remove (for Grub 0.9x)
grub_cmdline_remove_args: []
# Example:
#grub_cmdline_remove_args:
#  - biosdevname=0

# Default path to the Grub 0.9x default config file
grub_cmdline_path1: /boot/grub/grub.conf

# Default path to the Grub2 default config file
grub_cmdline_path2: /etc/default/grub
```

All changes are always applied to all configured kernels.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

N/A


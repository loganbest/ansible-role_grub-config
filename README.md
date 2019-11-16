grub-config
=========

This role modifies the GRUB defaults to how you'd like.

Requirements
------------


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

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
---
- hosts: packer
  roles:
    - role: grub
      grub_cmdline_add_args:
        - console=tty0
        - console=ttyS0,115200
```

License
-------

N/A


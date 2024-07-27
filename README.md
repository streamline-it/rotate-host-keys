Role Name
=========

Creates host keys for specified servers and rotates keys for all hosts specified

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

# Needed to point to the user's home directory.  Linux home directories are under /home.  FreeBSD for example is under /usr/home.

rotate_host_keys_userdir: path to home directory

# User account to isolate on
rotate_host_keys_user: username

# Host keys for target systems to log into
rotate_host_keys_target_hosts:
  - hostname: hostname
    username: usename
    homedir: path to home directoyr
    remote_dir: remote directory on the controller


Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - rotate-host-keys

License
-------

BSD

Author Information
------------------

streamline-it

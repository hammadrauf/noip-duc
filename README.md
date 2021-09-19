Role Name
=========

This role install the dynamic update client on a raspberry pi.

To start the client use the command: 

    /usr/local/bin/noip2

To reconfigure the client use the command:

    /usr/local/bin/noip2 -C

Requirements
------------

In order to work, gcc and the make tool must be installed.
Oterwise the role will install said utility.

Example Playbook
----------------

Installing the play

    ansible-galaxy install git+https://github.com/Mot93/rpi-install-noip-dynamic-update-client.git
    
Out of the box use:

    - hosts: raspberry
      remote_user: ubuntu
      become: yes
      roles:
        - rpi-install-noip-dynamic-update-client

License
-------

MIT

Author Information
------------------

If you like my work and whant to know more, visit my website:
[mattiarubini.com](https://mattiarubini.com)

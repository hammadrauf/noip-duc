Role Name
=========

This role install the dynamic update client on a raspberry pi.

The role follows the [official guide](https://www.noip.com/support/knowledgebase/install-ip-duc-onto-raspberry-pi/).

To start the client use the command: 

    /usr/local/bin/noip2

To reconfigure the client use the command:

    /usr/local/bin/noip2 -C

Requirements
------------

In order to work, gcc and the make tool must be installed.
Oterwise the role will install both utility.

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
        
Once the playbook has completed it's operation, login in the pi and execute the following commands:

    cd /home/pi/noip
    sudo make install
    
Once the configuration is completed, launche the following command to make sure that the agent runs at startup:
    
    sudo /usr/local/bin/noip2

To check the configuration simply run:

    sudo /usr/local/bin/noip2 -S
    
License
-------

MIT

Author Information
------------------

If you like my work and want to know more, visit my website:
[www.mattiarubini.com](https://www.mattiarubini.com)

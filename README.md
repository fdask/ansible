To kick off the process, we need a user on the remote machine with sudo access.
Then make sure we can log in using a key!

# ssh-copy-id user@machine

Probably want to use SSH Agent to remember the passphrase for the keys used.

# ssh-agent bash
# ssh-add 

To run the playbook, add the machine to /etc/hosts and issue the following command:

# ansible-playbook ./playbook.yml

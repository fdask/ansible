No website, nothing fancy.  A public repo of some uber basic playbooks for installing things with Ansible.
A lot done as a learning excercise, almost all on CentOS 5 or 6 so non rh derivatives may have problems.

Install Ansible first!

> yum install ansible python-setuptools

Now, to kick off the process, we need a user on the remote machine with sudo access.
Then make sure we can log in using a key!

> ssh-copy-id user@machine

Probably want to use SSH Agent to remember the passphrase for the keys used.

> ssh-agent bash
> ssh-add 

To run the playbook, add the machine to /etc/hosts and issue the following command:

> ansible-playbook -u REMOTE-USER ./playbook.yml

To run commands manually (ad-hoc mode), do something like this:

> ansible <machine> -a "command"

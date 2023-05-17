# ansible_playbooks
Repo Containing Ansible Playbooks

* Configure your hosts in the included hosts file.

* cd into this folder via terminal on your computer

To apply run: -

```ansible-playbook install-docker.yml --inventory-file=hosts -l GreyLog -u andrew```

In the above example - I target the install docker playbook, I set my inventory hosts file to the hosts file included in this repo/folder, target my inventory section in hosts called Greylog
I also set the user to andrew which is already configured on the remote host with ssh keys for this local machine Im working on in the authorized key file.
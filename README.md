# ansible_playbooks
Repo Containing Ansible Playbooks

* Configure your inventory in the included hosts file.

* cd into this folder via terminal on your computer

To apply run: -

```ansible-playbook install-docker.yml --inventory-file=hosts -l GreyLog -u andrew```

In the above example - I target the install docker playbook, I set my inventory hosts file to the hosts file included in this repo/folder, target my inventory section in hosts called Greylog
I also set the user to andrew which is already configured on the remote host with ssh keys for this local machine Im working on in the authorized key file.

## Plex Info ##
When setting up Plex which resides on a vm or different network:

If you’re on a different network than the server computer (or the entire “local network” is not in the private network IP ranges), you’ll first need to set up a SSH tunnel so that you can access things as if they were local.

Tip!: This is only necessary for the initial setup. Once you’ve gone through the setup, you can access as normal.

macOS or Linux
Open a Terminal window or your command prompt
Enter the following command (substituting the IP address of your server as appropriate):
``` ssh -L 8888:127.0.0.1:32400 ip.address.of.server ```
Open a browser window
Type ```http://127.0.0.1:8888/web ```into the address bar
The browser will connect to the server as if it were local and load Plex Web App.  

Continue your login and setup of plex.

Now try accessing your plex server by the proper ip address of your remote server. You should be able to login and use plex as normal.
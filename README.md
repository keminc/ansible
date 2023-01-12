This is example of using <b>Ansible</b>.

<b>What you can find</b>:
 1. How to install pakages
 2. How to upload files
 3. How to work with Roles and Playbooks

<b>How to use</b>:
In playbook forlder you can find all exemples.

<b>Commands</b>:
#run
ansible-playbook playbooks/roles.yml

#run with vars
ansible-playbook playbooks/roles.yml --extra-var='owner=Denis'

#print all variables for host
ansible all -m setup

#execute command
ansible all -m shell -a 'ls -l /'

#create roles
mkdir roles
cd roles/
ansible-galaxy init deplay_nginx_web
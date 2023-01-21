This is example of using <b>Ansible</b>.

<b>What you can find</b>:
 1. How to install pakages
 2. How to upload files
 3. How to work with Roles and Playbooks

<b>How to use</b>:
In playbook folder you can find all exemples.

<b>Commands</b>:
#run <br>
ansible-playbook playbooks/roles.yml

#run with vars <br>
ansible-playbook playbooks/roles.yml --extra-var='owner=Denis'

#print all variables for host <br>
ansible all -m setup

#execute command <br>
ansible all -m shell -a 'ls -l /'

#create roles <br>
mkdir roles <br>
cd roles/ <br>
ansible-galaxy init deplay_nginx_web

#Run vault playbook
ansible-playbook playbooks/vault.yml --ask-vault-pass #--vault-password-file passfile.txt

#Vault string
ansible-vault encrypt_string
echo -n 'Password01' | ansible-vault encrypt_string

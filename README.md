# mini Ansible guide

This is example of using <b>Ansible</b>.

<b>What you can find</b>:
 1. How to install pakages
 2. How to upload files
 3. How to work with Roles and Playbooks

<b>How to use</b>:
In playbook folder you can find all exemples.

<b>Commands</b>:<br><br>
Run playbook
```bash
ansible-playbook playbooks/roles.yml
```

Run with vars <br>
```bash
ansible-playbook playbooks/roles.yml --extra-var='owner=Denis'
```

Print all variables for host <br>
```bash
ansible all -m setup
```

Execute command <br>
```bash
ansible all -m shell -a 'ls -l /'
```

Create roles <br>
```bash
mkdir roles <br>
cd roles/ <br>
ansible-galaxy init deplay_nginx_web
```

Run vault playbook <br>
```bash
ansible-playbook playbooks/vault.yml --ask-vault-pass #--vault-password-file passfile.txt
```

Vault string <br>
```bash
ansible-vault encrypt_string <br>
echo -n 'Password01' | ansible-vault encrypt_string
```

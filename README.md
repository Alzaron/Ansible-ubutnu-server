1. add ip to server in /etc/ansible/inventory
   or make inventory in root of folder and change ansible.cfg   
2. make a ssh key for server .ssh/ansible and add to server  
3. Run `ansible-galaxy install -r requirements.yml`
4. Run `ansible-playbook playbook.yml -K`
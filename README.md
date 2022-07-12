1. Add IP of server to `/etc/ansible/inventory`
   or make inventory in root of folder and change `ansible.cfg`   
2. make a ssh key for server .ssh/ansible and add to server  
```sh
### Generate key
ssh-keygen -t ed25519 -C "Ansible"
```
```sh
### Copy key to server
ssh-copy-id -i ~/.ssh/yourkey.pub Ip_of_your_server
```

3. Run `ansible-galaxy install -r requirements.yml`
4. Run `ansible-playbook playbook.yml -K`  |
If not added ssh key run `ansible-playbook playbook.yml -kK` instead 
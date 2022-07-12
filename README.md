1. add ip to server in /etc/ansible/inventory
   or make inventory in root of folder and change ansible.cfg   
2. make a ssh key for server .ssh/ansible and add to server  
```sh
ssh-keygen -t ed25519 -C "Ansible default"
```
### copy key to server
```
ssh-copy-id -i ~/.ssh/yourkey.pub Ip_of_your_server
```
### login to server with key
```sh
ssh -i ~/.ssh/yourkey Ip_of_your_server

```
3. Run `ansible-galaxy install -r requirements.yml`
4. Run `ansible-playbook playbook.yml -K`
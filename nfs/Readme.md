#NFS client/server

In order to share an existing owncloud data using nfs.

It uses Ansible for provisioning and Vargrant for develoment.

##NFS server

- Install a nfs server in the inventory host
- Exposes owncloud folder by nfs

###How to use it

1. Setup your inventory accordingly to [http://docs.ansible.com/ansible/intro_inventory.html#inventory]

Current inventory defines two hosts humhum and owncloud


2. From the nfs folder (any other by adjusting the path)
```
ansible-playbook -vvvv -i nfs-server/inventories/nfs nfs-server/playbooks/nfs-server.yml
```
##NFS client

- Install and setup a nfs client in the inventory host
- Mounts owncloud folder

###How to use it

1. Setup your inventory accordingly to [http://docs.ansible.com/ansible/intro_inventory.html#inventory]

Current inventory defines two hosts humhum and owncloud


2. From the nfs folder (any other by adjusting the path)
```
- ansible-playbook -vvvv -i nfs-client/inventories/nfs nfs-client/playbooks/nfs-client.yml
```
##References




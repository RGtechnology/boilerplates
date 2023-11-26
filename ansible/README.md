# Ansible

[Ansible Documentation](https://docs.ansible.com/ansible/latest/getting_started/index.html)

... Ansible automates the management of remote systems and controls their desired state. A basic Ansible environment has three main components:
## Control node 
A system on which Ansible is installed. You run Ansible commands such as ansible or ansible-inventory on a control node.

## Managed node
A remote system, or host, that Ansible controls.

## Inventory
A list of managed nodes that are logically organized. You create an inventory on the control node to describe host deployments to Ansible.

### Commands

#### Inventory Graph
```
ansible-inventory -i inventories/example/hosts.yml --graph
```

```
ansible-inventory -i inventories/example/hosts.yml --graph --vars
```

#### Ping inventory
```
ansible all -m ping -i inventories/example/hosts.yml
```
#### Examples to execute playbooks
```
ansible-playbook playbooks/example-playbook.yml -i inventories/example/hosts.yml
```

```
ansible-playbook playbooks/example-playbook.yml
```

```
ansible-playbook playbooks/example-playbook.yml --limit debian12-test
```

```
ansible-playbook playbooks/example-playbook.yml --limit env_debian
```

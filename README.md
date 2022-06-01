## Cluster k3s com Ansible

Provisionamento de cluster k3s com Ansible. Inicialmente este playbook serve para provisionar um cluster com um master e N workers.



**Neste repositório tem um Vagrantfile que provisiona também as máquinas no VirtualBox**

Caso for usar apenas o playbook, você deverá criar um arquivo de inventario.
Exemplo:
```
[all]
k3s-master  ansible_host=192.168.56.10
k3s-worker2 ansible_host=192.168.56.20
k3s-worker3 ansible_host=192.168.56.30

[all:vars]
ansible_user=sysadmin

#Para autenticação SSH via senha [requer sshpass] use:
#ansible_password=vagrant

#Para autenticação via Private Key use:
#ansible_ssh_private_key_file='~/.ssh/sysadmin'

become_method=sudo
ansible_python_interpreter=/usr/bin/python3
```

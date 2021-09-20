Playbooks de automação para Vm's usando ansible.

Necessario ter instalado: 
	- Ansible
	- Virtualbox 
	- Vagrant

Para executar o script use o comando: 

```
vagrant up
```
e depois:

```
ansible-playbook playbook.yaml -i ./hosts <senha do usuario para o become>
```
Para parar: 

``` 
vagrant halt
````
Para destruir: 

```
vagrant destroy
```

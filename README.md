# How to run script

* First, change ip in segment master and backup of inventory hosts file
* Install ansible in deployment node
* Run playbook ***install_docker.yml*** to install requirement package
```sh
ansible-playbook -i /path/to/inventory /path/to/install_docker.yml
```
* Run playbook ***bootstrap_folder_docker.yml*** to create folder and config file
```sh
ansible-playbook -i /path/to/inventory /path/to/bootstrap_folder_docker.yml
```
* Run playbook ***restart_elastic.yml*** to change password for kibana and start service
```sh
ansible-playbook -i /path/to/inventory /path/to/bootstrap_folder_docker.yml
```
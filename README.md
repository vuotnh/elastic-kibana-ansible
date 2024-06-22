# How to run script

* Clone project to ***/root*** folder
* First, change ip in segment master and backup of inventory hosts file
* Install ansible in deployment node
* B1: Run playbook ***install_docker.yml*** to install requirement package
```sh
ansible-playbook -i /path/to/inventory /path/to/install_docker.yml
```
* B2: Run playbook ***general_task.yml*** to run general task
```sh
ansible-playbook -i /path/to/inventory /path/to/general_task.yml
```
* B3: Run playbook ***bootstrap_ca_elastic.yml***
```sh
ansible-playbook -i /path/to/inventory /path/to/bootstrap_ca_elastic.yml
```
* B4: Run playbook ***deploy_elasticsearch.yml***
```sh
ansible-playbook -i /path/to/inventory /path/to/deploy_elasticsearch.yml
```
* B5: Run playbook ***deploy_ha_kibana.yml***
```sh
ansible-playbook -i /path/to/inventory /path/to/deploy_ha_kibana.yml
```
* B6: Run playbook ***deploy_packetbeat.yml***
```sh
ansible-playbook -i /path/to/inventory /path/to/deploy_packetbeat.yml
```

* B7: SSH vào terminal của container packetbeat, chạy lệnh sau
```sh
packetbeat setup -e -E setup.kibana.host=https://<vip_ip>:5602 -E setup.kibana.ssl.verification_mode=none
```

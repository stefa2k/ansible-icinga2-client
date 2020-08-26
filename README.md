# ansible-icinga2-client

[Ansible](https://www.ansible.com/) playbook to set up icinga2 client.

## Requirements on the host(s)
* Linux with apt (Ubuntu)
* Configured icinga2 in docker (tba)

## Configuration
### Common variables
Variable | Description
---------|-------------
`master_satellite_node` | Master or satellite icinga2 node (Common Name)
`master_satellite_host` | IP of master or satellite icinga2 node
`master_satellite_port` | Port of master or satellite icinga2 node

### Host variables
Variable | Description | Mandatory
---------|-------------|----------
`icinga2_client_common_name` | Client's common name | Yes (if client); No (if master/satellite)

## Run
Example:
```
ansible-playbook -i inventory.yaml -l node1,node2,node3 icinga2-client.yaml
```

# Ansible Logstash Role 

This is a Ansible role to install Logstash (Support Ubuntu14/16, CentOS7)

## Requirements

Ansible 2.x

## Role Variables

|Variable|Default Value|Description|
|---|---|---|
```elasticsearch_address```|["127.0.0.1"]|elasticsearch address list
```elasticsearch_port```|9200|elasticsearch port


## Example
```
### create a requirements.yml
- src: git+https://github.com/willyhutw/ansible-role-logstash.git
  name: logstash

### create a playbook.yml
- hosts: all
  become: yes
  roles:
    - roles/logstash

### install this role
ansible-galaxy install -r requirements.yml -p ./roles

### run it!
ansible-playbook -i '192.168.33.101,' playbook.yml \
-e "ansible_ssh_user=willyhu ansible_ssh_pass=secret ansible_sudo_pass=secret" \
-e "{'elasticsearch_address':['192.168.33.101','192.168.33.102']}"
```

## License

MIT / BSD

## Author Information

willyhu.tw@gmail.com

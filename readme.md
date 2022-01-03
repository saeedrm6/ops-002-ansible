# Installing Ansible on control node manager

### Method 1: pip
```
apt install -y python3-pip python3-venv
python -m venv venv
source venv/bin/active
pip install wheel
pip install ansible
```

### Method 2: apt
```
apt install -y software-properties-common
apt-add-repository --yes --update ppa:ansible.ansible
apt install -y ansible
```

<hr>

### Defining hosts in hosts.ini
```
oops-002-ansible.saeed.cloud ansible_user=ubuntu
```

## ping defined nodes in hosts.ini
```
ansible all -i hosts.ini -m ping
```
## check & install docker
```
ansible-playbook -i hosts.ini playbook-docker.yaml
```

## check & install docker-compose
```
ansible-playbook -i hosts.ini playbook-dockercompose.yaml
```

## CI Robots
[@dwsclass](https://github.com/dwsclass) ops-002-ansible

## License

[APACHE LICENSE, VERSION2.0](https://www.apache.org/licenses/LICENSE-2.0)
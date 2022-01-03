# Installing Ansible on control node manager

### Method 1: pip
```
apt install -y python3-pip python3-venv
python -m venv venv
source venv/bin/active
pip install wheel
pip install ansible
```

###Method 2: apt
```
apt install -y software-properties-common
apt-add-repository --yes --update ppa:ansible.ansible
apt install -y ansible
```

<hr>

## ping defined nodes in hosts.ini
```
ansible all -i hosts.ini -m ping
```
## run playbook
```
ansible-playbook -i hosts.ini play.yaml
```
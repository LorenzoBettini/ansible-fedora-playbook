# ansible-fedora-playbook
Ansible playbooks for Fedora installations and configurations

ansible-galaxy install -r requirements.yml

ansible-playbook -i local -v playbook-fedora-gnome.yml -K

ansible -m include_tasks -a file=tasks/main-packages.yml localhost -K

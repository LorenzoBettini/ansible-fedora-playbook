# ansible-fedora-playbook
Ansible playbooks for Fedora installations and configurations

ansible-playbook -i local -v show-linux-distro-details.yml

ansible-galaxy install -r requirements.yml
ansible-galaxy collection install -r requirements.yml

ansible-playbook -i local -v playbook-fedora-gnome.yml -K

ansible-playbook -i local -v test-tasks-playbook.yml -K

ansible -m include_tasks -a file=tasks/main-packages.yml localhost -K

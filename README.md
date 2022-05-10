# ansible-fedora-playbook
Ansible playbooks for Fedora installations and configurations

Enable RPM fusion

sudo dnf install \
https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

sudo dnf install \
https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

ansible-playbook -i local -v show-linux-distro-details.yml

ansible-galaxy install -r requirements.yml
ansible-galaxy collection install -r requirements.yml

ansible-playbook -i local -v playbook-fedora-gnome.yml -K

ansible -m include_tasks -a file=tasks/main-packages.yml localhost -K

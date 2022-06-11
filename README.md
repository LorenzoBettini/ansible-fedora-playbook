# ansible-fedora-playbook
Ansible playbooks for Fedora installations and configurations

Install requirements

```
ansible-galaxy collection install -r requirements.yml
ansible-galaxy install -r requirements.yml
```

Run a playbook, e.g., for GNOME

```
ansible-playbook -i local -v playbook-fedora-gnome.yml -K
```

In case, you can skip a few steps, e.g., `--skip-tags latex`.

For local quick testing of single tasks, include them in `test-tasks-playbook.yml` and then:

```
ansible-playbook -i local -v test-tasks-playbook.yml -K
```

For looking at distro details:

```
ansible-playbook -i local -v show-linux-distro-details.yml
```

For single tasks, specify the name of the task file, e.g.:

```
ansible -m include_tasks -a file=tasks/main-packages.yml localhost -K
```

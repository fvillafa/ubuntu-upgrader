# ubuntu-upgrader
Ansible playbook to upgrade an ubuntu installation

This silly playbook is to update/upgrade a Debian/Ubuntu installation.

Originally I was passing variables in the KEY=VALUE format, as in:
```
ansible-playbook -i localhost, ubuntu-upgrader.yml -K -e "apt_dist_upgrade=true apt_autoremove=true"
```

But decided to experiment with JSON format.

```
ansible-playbook -i localhost, ubuntu-upgrader.yml --extra-vars "@variables.json"
```

Soon I'll convert this to a role and add support for rpm based systems too (As I think there are fewer options for those).

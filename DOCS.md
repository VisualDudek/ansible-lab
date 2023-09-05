

### Folder structure

```txt
ansible-project/
├── inventories/
│   ├── production/
│   │   ├── hosts.ini
│   │   └── group_vars/
│   │       ├── all.yml
│   │       ├── web_servers.yml
│   │       └── db_servers.yml
│   ├── staging/
│   │   ├── hosts.ini
│   │   └── group_vars/
│   │       ├── all.yml
│   │       ├── web_servers.yml
│   │       └── db_servers.yml
├── playbooks/
│   ├── site.yml
│   ├── web_servers.yml
│   └── db_servers.yml
├── roles/
│   ├── common/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   ├── templates/
│   │   ├── files/
│   │   ├── vars/
│   │   └── handlers/
│   ├── web_server/
│   │   ├── tasks/
│   │   ├── templates/
│   │   ├── files/
│   │   ├── vars/
│   │   └── handlers/
│   └── db_server/
│       ├── tasks/
│       ├── templates/
│       ├── files/
│       ├── vars/
│       └── handlers/
├── library/
├── filter_plugins/
└── ansible.cfg
```
Here's a breakdown of the structure:

1. inventories/: This folder contains your inventory files, which list the hosts and groups of hosts Ansible will manage. It's divided into subfolders for different environments (e.g., production, staging).

2. playbooks/: This is where you store your playbook files. Playbooks define the tasks to be executed on a set of hosts.

3. roles/: Roles are reusable units of work in Ansible. Each role has its own directory structure containing tasks, templates, files, variables, and handlers specific to that role.

4. library/: This is where you can store custom Ansible modules that you've developed.

5. filter_plugins/: If you've created custom Jinja2 filters, you can place them here.

6. ansible.cfg: The Ansible configuration file for your project.
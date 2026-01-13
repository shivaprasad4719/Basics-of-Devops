# Ansible Basics 🚀
Ansible is an open-source automation tool used for configuration management, application deployment, and infrastructure automation.
It uses YAML for writing playbooks and works over SSH, so no agent is required on managed nodes.

# Why Ansible?
- Agentless architecture (uses SSH)
- Simple YAML syntax
- Idempotent (safe to run multiple times)
- Easy to learn and powerful for automation
- Widely used in DevOps & Cloud environments

# Ansible Architecture
- Control Node
  - The machine where Ansible is installed and playbooks are executed.
- Managed Nodes
  - Servers/instances managed by Ansible via SSH.
- Inventory
  - List of managed nodes (static or dynamic).
- Playbooks
  - YAML files that define automation tasks.
---
# Ansible Components
# 1. Inventory
 - Defines hosts and groups.
<pre>
[web]
192.168.1.10
192.168.1.11

[db]
192.168.1.20
</pre>
# 2. Modules
- Reusable units of work (package, service, copy, user, etc.).
- Examples:
  - yum
  - apt
  - service
  - copy
  - file
# 3. Playbook
- A set of tasks executed on target hosts.
---
<pre> 
# Ex:
- name: Install Apache Web Server
  hosts: web
  become: yes
  tasks:
    - name: Install httpd
      yum:
        name: httpd
        state: present

    - name: Start Apache service
      service:
        name: httpd
        state: started
        enabled: yes
</pre>
# 4. Roles
- A structured way to organize playbooks.
<pre>
roles/
├── webserver/
│   ├── tasks/
│   │   └── main.yml
│   ├── handlers/
│   ├── templates/
│   ├── files/
│   └── vars/
</pre>
---
# Common Ansible Commands
# Check Ansible version
- ansible --version

# Ping all hosts
- ansible all -m ping

# Run ad-hoc command
- ansible web -m yum -a "name=httpd state=present" -b

# Run playbook
- ansible-playbook site.yml
---
# Ansible Playbook Structure
<pre>
- hosts: all
  become: yes
  vars:
    pkg_name: nginx
  tasks:
    - name: Install package
      apt:
        name: "{{ pkg_name }}"
        state: present
</pre>
# Ansible Best Practices
- Use roles for large projects
- Use variables instead of hard-coding values
- Keep inventory organized
- Use handlers for service restarts
- Use Ansible Vault for secrets
  
# Use Cases
- Server configuration
- Application deployment
- Patch management
- Cloud automation (AWS, Azure, GCP)
- CI/CD pipeline integration

# Who Should Learn Ansible?
- DevOps Engineers
- Cloud Engineers
- System Administrators
- SREs
---
# Author
Shiva V
AWS & DevOps Engineer
📌 Learning • Automating • Building

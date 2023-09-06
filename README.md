# Ansible Lab Repository

Welcome to my private Ansible lab repository! This repository is designed to help me learn and experiment with Ansible, an open-source automation tool for configuring and managing systems.

## Table of Contents

- [About Ansible](#about-ansible)
- [Lab Setup](#lab-setup)
- [Usage](#usage)
- [Examples](#examples)
- [Resources](#resources)
- [License](#license)

## About Ansible

Ansible is a powerful automation tool that allows you to automate configuration management, application deployment, and other IT tasks. It uses a simple YAML-based syntax for defining tasks, playbooks, and roles, making it easy to learn and use.

## Lab Setup

Before you begin, ensure that you have the following prerequisites:

- Ansible installed on your local machine.
- OR setup Python virtual env using `pyenv` from `requirements.txt`

### AWS

- Setup your AWS credential e.g. using `leapp`
- Create/Import into EC2 Key Pairs your ssh key
- Provide into `cfn-ec2-stack.yaml` Key pair name AND region specific AMI IDs
- Make sure that in `inventory.aws_ec2.yaml` you have correct region
- Deploy cfn stack using `rain`
- Test inventory via `ansible-inventory -i [path_to_aws_dyna_inventory_file]`
- Test connectivity via `ping.yaml` playbook

## Usage
Update the inventory file (inventory.yml) with the IP addresses or hostnames of the remote machines you want to manage using Ansible.

Write playbooks in YAML format to define tasks you want to execute on remote machines.

Execute playbooks using the ansible-playbook command. For example:

```bash
ansible-playbook -i inventory.yml playbook.yml
```

## Examples
In this repository, you'll find various example playbooks and roles to help you get started:

playbook.yml: An example playbook showcasing basic Ansible tasks.
webserver-role/: An example role for setting up a basic web server.
database-role/: An example role for configuring a database server.
Feel free to modify and expand upon these examples to suit your learning and testing needs.

## Resources
Here are some helpful resources to learn more about Ansible:

- [Ansible Documentation](https://docs.ansible.com/)
- [Ansible Galaxy](https://galaxy.ansible.com/): A repository for sharing Ansible roles.
- [Ansible Community](https://ansible.community/): Join the Ansible community to ask questions and share knowledge.

## License
This repository is licensed under the MIT License.

Copyright 2023 Marcin Dudek

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.